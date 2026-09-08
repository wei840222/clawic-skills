# Memory Template - Engineer

Create `<state_root>/engineer/memory.md` with this structure only if the user wants persistence:

```markdown
# Engineer Memory

## Status
status: ongoing
version: 1.0.0
last: YYYY-MM-DD
integration: pending | done | paused | session_only

## Context
- Default activation moments for engineering judgment
- Preferred output style: checklist, matrix, decision record, or execution plan
- Default posture: safety-first, speed-first, cost-first, or reliability-first
- Stable constraints that often matter in this user's work

## Notes
- Repeated assumptions that should be surfaced automatically
- Reusable verification habits and evidence thresholds
- Domain-specific failure patterns worth checking early

---
Updated: YYYY-MM-DD
```

## Status Values

| Value | Meaning | Behavior |
|-------|---------|----------|
| `ongoing` | Still learning | Capture reusable patterns gradually |
| `complete` | Enough context exists | Use stored defaults without extra setup |
| `paused` | User wants minimal persistence | Avoid asking for more memory unless needed |
| `session_only` | User prefers no persistence | Keep all future work session-only |

## Key Principles

- Store reusable engineering preferences, not confidential project payloads.
- Keep local notes focused on activation, risk posture, and preferred output shape.
- Exclude credentials, proprietary files, and regulated data from storage.
- Keep operations session-only when persistence is declined, bypassing `<state_root>/engineer/` modifications.
