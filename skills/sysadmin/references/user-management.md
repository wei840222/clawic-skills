# User Management

- Create service accounts with `--system` flag — no home directory, no login shell
- Grant `sudo` access only for required specific commands — principle of least privilege
- Lock accounts instead of deleting: `usermod -L` — preserves audit trail and file ownership
- SSH keys in `~/.ssh/authorized_keys` with restrictive permissions — 600 for file, 700 for directory
- `visudo` to edit sudoers — catches syntax errors before saving, prevents lockout
