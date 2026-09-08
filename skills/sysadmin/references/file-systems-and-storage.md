# File Systems and Storage

- `df -h` for disk usage, `du -sh *` to find culprits — check before disk fills completely
- `lsof +D /path` finds processes using a directory — needed before unmounting
- `ncdu` for interactive disk usage — faster than repeated du commands
- Mount options matter: `noexec`, `nosuid` for security on data partitions
- Resize filesystems with care: grow is safe, shrink risks data loss — always backup first
