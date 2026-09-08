# Common Traps - Engineer

## Scope creep into implementation

**Trap:** Jumping from constraints and failure modes straight into code, scripts, or vendor configuration.

**Better:** Keep this skill on boundaries, options, risks, and verification. Route implementation to `software-engineer` (or the domain skill) after the plan is stable.

## Hidden assumptions

**Trap:** Treating unstated load, staffing, safety, schedule, or interface assumptions as facts.

**Better:** Write assumptions into the decision record. Mark which ones block the recommendation and which ones can be revised after the first verification rung.

## Solution-first framing

**Trap:** Naming a preferred design before the system boundary, success criteria, and hard constraints are clear.

**Better:** Restate the problem, envelope, and non-negotiables first. Only then score options against those constraints.

## Verification theater

**Trap:** Listing tests that do not prove the actual risk (for example, unit checks when the failure is operational handoff).

**Better:** Climb the verification ladder from cheapest decisive evidence to higher-cost proof. Tie each check to a failure mode or acceptance criterion.

## Persistence without consent

**Trap:** Writing durable notes under `<state_root>/engineer/` before the user asks for memory.

**Better:** Default to session-only work. Ask once, in plain language, before creating local engineering memory, and never store credentials or proprietary payloads.

## Over-collecting context

**Trap:** Interrogating for preferences and history that do not change the current decision.

**Better:** Ask only for details that flip the recommendation. Capture stable defaults later, after the immediate answer is useful.
