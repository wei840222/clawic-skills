# Setup - Real Estate Investing

Use this file when the user wants investing help to become a recurring capability and `<state_root>` has been resolved according to `SKILL.md`.

Answer the immediate deal question first, then lock activation behavior early so future investing conversations start with the right guardrails instead of re-learning the same context.

## Immediate First-Run Actions

### 1. Lock integration behavior early

Within the first exchanges, clarify:
- should this activate whenever the user talks about rental property, underwriting, cap rate, BRRRR, flips, or buying to invest
- should it jump in proactively when a property opportunity appears or only on explicit request
- whether owner-occupant deals with partial investment intent should load this skill, `home-buying`, or both

Keep this brief. One clear integration question is enough.

### 2. Lock the user's investing frame

Understand the basics that change every decision:
- preferred strategy: buy-and-hold, value-add, BRRRR, flip, house hack, short-term rental, or "still exploring"
- capital range and financing comfort
- target geography or markets already being considered
- what matters most right now: cash flow, equity growth, speed, simplicity, tax efficiency, or learning

Do not interrogate. Start broad, then narrow only where the current decision needs it.

### 3. Lock boundaries and storage scope

Clarify:
- what should be remembered across deals: target markets, budget ceiling, minimum return, risk tolerance, asset types, management preference
- what should stay out of memory: tax IDs, lender logins, full legal documents, account numbers, or highly sensitive personal details
- whether exact addresses may be stored or only shorthand references

### 4. Create local state only after the routing contract is clear

```bash
mkdir -p "<state_root>/archive"
touch "<state_root>/memory.md"
touch "<state_root>/pipeline.md"
touch "<state_root>/markets.md"
touch "<state_root>/decisions.md"
chmod 700 "<state_root>" "<state_root>/archive"
chmod 600 "<state_root>/memory.md" "<state_root>/pipeline.md" "<state_root>/markets.md" "<state_root>/decisions.md"
```

If the files are empty, initialize them from `references/memory-template.md`.

### 5. What to save

Save only what improves future investment decisions:
- activation behavior and whether this should load proactively
- thesis, buy box, and return guardrails
- market notes that recur across deals
- active opportunities, blockers, and next diligence steps
- post-mortems on passed, lost, and closed deals

Do not store secrets, banking credentials, tax IDs, or full legal packages.
