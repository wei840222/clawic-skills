# Networking Basics

- `ss -tulpn` shows listening ports — `netstat` is deprecated
- `ip addr` and `ip route` replace `ifconfig` and `route` — learn the new tools
- Check both host firewall and cloud security groups — traffic blocked at either level fails
- `/etc/hosts` for local overrides — quick testing without DNS changes
- `curl -v` shows full connection details — headers, timing, TLS handshake
