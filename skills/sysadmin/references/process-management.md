# Process Management

- Use `systemctl` for services rather than legacy tools — systemd is standard on modern distros
- `journalctl -u service -f` for live logs — more powerful than tail on log files
- `nice` and `ionice` for background tasks — ensure production workloads receive priority
- Kill signals: SIGTERM (15) first, SIGKILL (9) last resort — SIGKILL doesn't allow cleanup
- `nohup` or `screen`/`tmux` for long-running commands — SSH disconnect kills regular processes
