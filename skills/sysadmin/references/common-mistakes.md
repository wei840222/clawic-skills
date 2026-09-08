# Common Mistakes

- Running services as root — one exploit owns the system
- Establish monitoring before incidents — proactive signals reduce recovery cost
- Editing config without backup — `cp file file.bak` takes two seconds
- Diagnose the root cause before rebooting; record evidence so the issue can be resolved
- Ignoring disk space warnings — 100% full causes cascading failures
- Forgetting timezone configuration — without it, logs from different servers will fail to align correctly
