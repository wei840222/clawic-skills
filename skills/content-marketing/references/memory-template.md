# Memory Template — Content Marketing

Create `<state_root>/memory.md` with this structure:

```markdown
# Content Marketing Memory

## Status
status: ongoing
version: 1.0.0
last: YYYY-MM-DD
integration: pending

## Strategy
<!-- Approved objectives, audience, offers, channels, and success metrics -->

## Voice
<!-- Approved tone, style, preferred terms, restricted terms, and examples -->

## Current Focus
<!-- Current campaign, owner, deadlines, and next review date -->

## Notes
<!-- Evidence, hypotheses, decisions, and unresolved questions -->

---
*Updated: YYYY-MM-DD*
```

## Status Values

| Value | Meaning | Behavior |
|-------|---------|----------|
| `ongoing` | Discovery is incomplete | Request only the next decision needed for the active brief |
| `complete` | Approved context is sufficient | Execute against the approved brief |
| `paused` | User deferred discovery | Use existing approved context and label assumptions |
| `never_ask` | User requested no discovery prompts | Use existing approved context and accept only volunteered updates |

## Calendar Template

Create `<state_root>/calendar.md`:

```markdown
# Editorial Calendar

## This Week
| Day | Content | Type | Funnel | Status | Channel |
|-----|---------|------|--------|--------|---------|

## Next Week
| Day | Content | Type | Funnel | Status | Channel |
|-----|---------|------|--------|--------|---------|

## Content Bank
<!-- Ideas to develop -->
-
-
-

---
*Updated: YYYY-MM-DD*
```

## Key Principles

- Record only approved, task-relevant information.
- Keep assumptions distinct from user-provided facts.
- Update `last` when persistent state changes.
