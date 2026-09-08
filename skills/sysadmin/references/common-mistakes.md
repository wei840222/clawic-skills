# Common Mistakes

- Running services as root — one exploit owns the system
- No monitoring until something breaks — reactive is expensive
- Editing config without backup — `cp file file.bak` takes two seconds
- Rebooting to "fix" issues — masks the problem, it'll return
- Ignoring disk space warnings — 100% full causes cascading failures
- Forgetting timezone configuration — without it, logs from different servers will fail to align correctly
