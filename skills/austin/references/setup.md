# Setup — Austin

## Philosophy

**This skill works from minute zero.** No blocking setup ritual.

Answer the user's question first. Always. Optional continuity happens only when it helps.

## On First Persistent-Memory Use

### Priority #1: Answer the ask

Whatever they asked about Austin, answer it with the right `references/` file. You do not need a full profile to be useful.

### Priority #2: Offer optional continuity once

Ask once, naturally, only if multi-turn Austin planning is likely:

> Want me to keep light Austin notes under your local skill state so later questions remember neighborhood/budget context?

If yes:

1. Resolve `<state_root>` per `SKILL.md`.
2. Explain the planned path (`<state_root>/austin/memory.md`) in plain language.
3. Create the file from `references/memory-template.md` only after confirmation.
4. Optionally note in the user's broader memory that the Austin skill is active — only if they want that cross-link.

If no, record `integration: declined` inside Austin memory only when a memory file already exists; otherwise simply stay stateless.

## Context to Gather Over Time

Learn gradually when relevant:

- Visiting, relocating, or already local?
- Industry / commute constraints?
- Housing budget band?
- Car vs transit preference?
- Neighborhoods already on a shortlist?
- Heat, allergy, school, or visa constraints?

Do not run a questionnaire up front.

## Status Values

| Status | When to use |
|--------|-------------|
| `ongoing` | Default. Still learning about their Austin journey. |
| `complete` | Situation is well known and stable. Rare. |
| `paused` | User deferred deeper questions. |
| `never_ask` | User asked to stop preference probing. |

## Golden Rule

If the user feels they must "set up" the skill before it helps, the design failed.

Be useful immediately. Learn only with consent.
