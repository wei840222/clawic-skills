# Performance

- `top`/`htop` for live view, `vmstat` for trends — understand baseline before diagnosing
- `iotop` for disk I/O bottlenecks — slow disk often blamed on CPU
- Load average: 1.0 per core is healthy — consistently higher means queuing
- Swap usage isn't inherently bad — but consistent swapping indicates memory shortage
- `sar` for historical data — retroactively diagnose what happened during incident
