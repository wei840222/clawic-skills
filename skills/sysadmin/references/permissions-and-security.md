# Permissions and Security

- `chmod 600` for secrets, `640` for configs, `644` for public — ensure world-writable permissions are omitted unless explicitly required
- Sticky bit on shared directories (`chmod +t`) — users can only delete their own files
- `setfacl` for complex permissions — when traditional owner/group/other isn't enough
- `chattr +i` makes files immutable — even root can't modify without removing flag
- SELinux/AppArmor in enforcing mode — permissive logs but doesn't protect
