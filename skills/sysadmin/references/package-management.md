# Package Management

- `apt update` before `apt upgrade` — upgrade without update uses stale package lists
- Unattended security updates: `unattended-upgrades` — critical patches shouldn't wait
- Pin package versions in production — unexpected upgrades cause unexpected outages
- Remove unused packages: `apt autoremove` — reduces attack surface and disk usage
- Know your package manager: apt/yum/dnf/pacman — commands differ, concepts similar
