---
name: roleplay
description: Run persistent fictional-character roleplay and structured practice scenarios with activation, coaching, and feedback. Use when a user asks to create or activate a character, rehearse a professional conversation, replay a scene, or receive roleplay feedback.
metadata:
  version: "1.0.0"
  openclaw: '{"emoji":"🎭"}'
---

## State location

Before the first state operation, resolve one `<state_root>`:

1. Use an explicitly configured state root when supplied by the user or host.
2. Otherwise use the first existing directory in this order: `<workspace>/roleplay/`, `<workspace>/memory/roleplay/`, then `~/roleplay/`.
3. If none exists and the user wants persistent roleplay data, create `<workspace>/roleplay/`.

Keep the selected root for the invocation. When more than one candidate exists, use only the highest-precedence directory and tell the user; do not merge or synchronize copies.

State under `<state_root>/`:
- `characters/` — character profiles; create when a character is saved.
- `scenarios/` — saved scenario templates; create when the user saves one.
- `sessions/` — session logs and feedback; create when the user asks to retain them.
- `active` — active-character marker; create only when activation must persist across sessions.

## Core workflow

1. Confirm the requested character or scenario and whether the user wants state saved.
2. For a real-person request, load `references/safeguards.md` before creating dialogue or a profile.
3. Resolve `<state_root>` before reading or writing any saved roleplay data.
4. Load the applicable reference from the router, then establish the character, scenario stakes, and desired difficulty.
5. During an active scene, keep the agreed character boundaries and track material turns. On `pause` or `coach me`, give coaching; on `deactivate`, `normal mode`, or an explicit end, return to normal behavior and save only consented notes.

## Situation router

| When to load | Resource |
| --- | --- |
| Create, edit, archive, or activate a character | `references/characters.md` |
| Practice medical, business, coaching, creative, or game scenarios | `references/scenarios.md` |
| Pause, replay, drills, difficulty changes, or post-session feedback | `references/practice.md` |
| Roleplay involving a living, deceased, or fictional real-world identity | `references/safeguards.md` |
| Review progress, recurring patterns, or workspace hygiene | `references/feedback.md` |

## Character profile

A saved profile includes a name or archetype, type, 3–5 core traits, speech patterns, background, relationship stance, behavioral tendencies, and session memory. Use `references/characters.md` for the full structure.
