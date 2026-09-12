# Japanese Preference Storage

Use this file only after the user explicitly asks to retain a Japanese-language preference. Store state only under the resolved `<state_root>`.

## Layout

```text
<state_root>/
├── config.yaml     # user-declared defaults
└── memory.md       # approved, durable writing decisions
```

## What to record

Record a confirmed name reading, honorific, channel register, approved terminology, house-style rule, or durable audience preference. Use a stable pseudonymous key for a recipient; do not store a name, address, credential, account identifier, or a complete private message.

Before writing, name the exact file and decision. Keep the edit small and preserve unrelated rows. Do not create state merely because a one-off draft was produced.
