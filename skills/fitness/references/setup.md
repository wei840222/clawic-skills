# Setup — Fitness

Read this on first use to load user preferences. Use existing data without prompting the user.

## Your Attitude

Consistency beats optimization. Your job is a plan the user will actually follow, adjusted from their log, not the theoretically best program. Be concrete: every prescription in Rule 8 form, every adjustment traceable to a logged number.

## How To Load Preferences

1. Read `<state_root>/fitness/config.yaml` if it exists. Apply its values.
2. For anything absent, use the defaults in the Configuration table of `SKILL.md` — assume defaults until overridden.
   - `units: metric`, `training_days: 3`, `session_minutes: 60`, `equipment: full-gym`, `primary_goal: general`, `age: none`, `measured_hrmax: none`.
   - For HR-zone math, source `age` from `config.yaml`, else optional shared profile age when available; `measured_hrmax` overrides both. If age and measured max are absent, use the talk test instead of estimating an age (SKILL.md Rule 5).
3. Read `<state_root>/fitness/memory.md` for baselines and history (e1RMs, resting HR, attendance, exclusions). Absence is fine; run `assessment.md` inside the normal flow of work instead.
4. Read the recent tail of `<state_root>/fitness/log.md` before prescribing — the next load comes from the last logged session (Output Gates).

Work from defaults immediately. Infer goals, schedule, and equipment implicitly from user statements; begin applying defaults immediately.

## Recording Preferences (only when the user declares one)

Write to config or memory **only** when the user states a preference in the course of the work — store data only as it naturally emerges in conversation.

- User names units, available days, session length, equipment, a goal, their age, or a measured HRmax → update the matching key in `<state_root>/fitness/config.yaml`.
- User expresses a schedule constraint, movement exclusion, risk stance, wearable in use, or coaching-style wish → record it under the matching preference area (schedule, exclusions, risk posture, data sources, coaching register) in `<state_root>/fitness/memory.md`.
- User reports a session, a bodyweight, or a wearable reading → append to `log.md`; recompute derived baselines in `memory.md` when they shift (`tracking.md`).
- User corrects earlier guidance → update the stored value to prevent redundant guidance.

If the user has said nothing, store nothing.

## What Memory Holds

See `memory-template.md` for the file formats. Track derived baselines (e1RM per lift, resting HR, attendance rate), observed context (schedule reality vs plan, equipment actually available), injury history and exclusions, and how much explanation they want — but only from what they actually reveal. A stated preference in `config.yaml` always outranks an observation in `memory.md`.
