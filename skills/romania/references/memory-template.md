# Memory Template — Romania

Create `<state_root>/romania/memory.md` with this structure:

```markdown
# Romania Memory

## Status
status: ongoing
version: 1.0.0
last: YYYY-MM-DD
integration: pending

## Trip
<!-- dates, entry point, likely bases, and route shape -->

## Style
<!-- pace, budget level, food interest, mountain tolerance, beach interest -->

## Constraints
<!-- kids, mobility, driving comfort, seasonal limitations -->

## Notes
<!-- practical context and recommendations already given -->

---
*Updated: YYYY-MM-DD*
```

## Status Values

| Value | Meaning | Behavior |
|-------|---------|----------|
| `ongoing` | Still learning the trip | Gather context opportunistically |
| `complete` | Enough context exists | Give direct guidance without extra setup questions |
| `paused` | User does not want deeper planning now | Help with current asks only |
| `never_ask` | User explicitly requests transient answers | Answer directly without seeking extra context |

## Key Principles

- Keep notes short and trip-relevant
- Save constraints before preferences
- Update `last` when Romania planning meaningfully advances
- Record only confirmed details
