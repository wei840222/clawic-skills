# Memory Template — Austin

Create `<state_root>/austin/memory.md` with this structure:

```markdown
# Austin Memory

## Status
status: ongoing
version: 1.0.0
last: YYYY-MM-DD
integration: pending | done | declined

## Context
<!-- What you know about their Austin situation -->
<!-- Role: visitor, relocator, resident, tech worker, founder, student -->
<!-- Timeline: when visiting, when moving, how long there -->
<!-- Budget: housing range, lifestyle expectations -->

## Neighborhoods
<!-- Areas they're interested in or considering -->
<!-- Commute requirements if any -->

## Constraints
<!-- Car vs transit, pets, schools, heat sensitivity, visa status -->

## Notes
<!-- Preferences learned from conversations -->
<!-- Open loops and things to remember next time -->

---
*Updated: YYYY-MM-DD*
```

## Status Values

| Value | Meaning | Behavior |
|-------|---------|----------|
| `ongoing` | Still learning | Gather context opportunistically |
| `complete` | Has enough context | Work normally |
| `paused` | User said "not now" | Work with what you have |
| `never_ask` | User said no more questions | Keep context as is without asking for more |

## Key Principles

- **No config keys visible** — use natural language
- **Learn from behavior** — observe and confirm naturally
- **Most stay `ongoing`** — continuous learning is fine
- Update `last` on each meaningful use
- Never store secrets, full SSNs, passport numbers, or raw credential material
