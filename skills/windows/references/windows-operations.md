# Windows Operational Details

## Credential Management

- Prefer Windows Credential Manager or a secrets backend over plaintext in scripts.
- Store generic credentials with `cmdkey` only when that is the approved local pattern:

  ```powershell
  cmdkey /generic:"MyService" /user:"admin" /pass:"<secret>"
  ```

- Retrieve with an approved helper (for example the `CredentialManager` module's `Get-StoredCredential`) or an org-standard vault API. Do not invent cmdlets that are not installed.
- For per-user encrypted local scripts:

  ```powershell
  $cred = Get-Credential
  $cred | Export-Clixml -Path "cred.xml"  # encrypted to current user/machine
  $cred = Import-Clixml -Path "cred.xml"
  ```

- `Export-Clixml` protection does not travel across machines or other users. Never commit `cred.xml` or secrets.

## Silent Failures

- Windows Defender may quarantine downloaded scripts/executables — check quarantine if a file disappears.
- Group Policy can override local settings quietly — use `gpresult /r` (or Resultant Set of Policy) to see what is actually applied.
- Antivirus real-time scanning can block file operations intermittently — add approved exclusions only for build/automation folders that policy allows.
- Prefer `-ErrorAction Stop` and explicit handling over `-ErrorAction SilentlyContinue` on control paths.
- Execution policy and unsigned scripts can fail with opaque errors on locked-down hosts — confirm policy with `Get-ExecutionPolicy -List`.

## Symbolic Links

- Creating symlinks requires admin **or** `SeCreateSymbolicLinkPrivilege`; regular users often fail without a clear message.
- Developer Mode can allow symlinks without full admin: Settings → System → For developers → Developer Mode.
- `mklink` is CMD-only; PowerShell uses `New-Item -ItemType SymbolicLink`.

## Script Signing

- On AllSigned / restricted hosts, sign production scripts:

  ```powershell
  $cert = Get-ChildItem Cert:\CurrentUser\My -CodeSigningCert
  Set-AuthenticodeSignature -FilePath script.ps1 -Certificate $cert
  ```

- AllSigned applies to profiles too (`$PROFILE`), not only the main script.

## Operational Safety

- Always dry-run destructive operations first: `Remove-Item -Recurse -WhatIf`.
- Use `Start-Transcript` when an audit trail is needed for incident review.
- NTFS ACLs via `icacls` have non-obvious inheritance — test on a copy before production paths.

## WinRM Remoting

- `Enable-PSRemoting -Force` is not enough on workgroups.
- Workgroup clients need TrustedHosts (scope narrowly):

  ```powershell
  Set-Item WSMan:\localhost\Client\TrustedHosts -Value "server1,server2"
  ```

- Prefer HTTPS remoting with proper certificates; HTTP can expose credentials on the network depending on auth configuration.
- Confirm the remote identity and endpoint before bulk commands.

## Event Logging

- Application-facing automation should log to Windows Event Log when central monitoring expects it:

  ```powershell
  New-EventLog -LogName Application -Source "MyScript" -ErrorAction SilentlyContinue
  Write-EventLog -LogName Application -Source "MyScript" -EventId 1000 -Message "Started"
  ```

- Creating a new event source typically needs elevation — do it at install time, not on every run.
- `-ErrorAction SilentlyContinue` on source creation is only for the “already exists” case; other failures should still be visible.

## File Locking

- Windows locks files aggressively. Probe before assuming a write path is free:

  ```powershell
  try { [IO.File]::OpenWrite($path).Close(); $true } catch { $false }
  ```

- Concurrent scheduled tasks and interactive users writing the same path conflict — use unique temp files and atomic replace.

## Temp File Hygiene

- `$env:TEMP` fills silently. Always clean up:

  ```powershell
  $tmp = New-TemporaryFile
  try {
    # work
  } finally {
    Remove-Item $tmp -Force -ErrorAction SilentlyContinue
  }
  ```

- Unlike many Linux `/tmp` policies, orphaned Windows temp files can survive reboots.

## Service Account Gotchas

- Services and many scheduled tasks run as a different principal than the logged-on user.
- `$env:USERPROFILE` under SYSTEM/service accounts points at the service profile, not the interactive user.
- Network access from SYSTEM uses machine credentials and may fail where the user succeeds.
- Mapped drives often do not exist for services — use UNC paths `\\server\share`.
