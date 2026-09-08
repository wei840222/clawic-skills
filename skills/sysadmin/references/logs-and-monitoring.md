# Logs and Monitoring

- `logrotate` prevents disk fill — configure size limits and retention
- Centralize logs to external system — local logs lost if server dies
- `/var/log/auth.log` or `/var/log/secure` for login attempts — watch for brute force
- `dmesg` for kernel messages — hardware errors, OOM kills appear here
- Monitor inode usage, along with overall disk space — many small files exhaust inodes
