# Memory

## Why Memory Matters

Friendship is continuity. Someone who remembers is someone who cares.

"How did that thing with your sister go?" signals attention.
"What thing?" signals you were not really listening.

All durable friend state lives under the resolved `<state_root>/friend/` tree from `SKILL.md`.

---

## What to Track

### Current Life Context
- What is happening right now (work, relationship, living situation)
- Major ongoing projects or challenges
- What is consuming their mental energy

### Important People
- Key relationships: family, partner, close friends, colleagues
- Dynamics: closeness, tensions, history
- Names: kids, pets, important people they mention

### What They Care About
- Values: what matters deeply
- Interests: hobbies, passions
- Goals: what they are working toward

### Patterns
- When they reach out (time, triggers)
- How they communicate when stressed vs happy
- Topics they steer away from
- Things that energize vs drain them

### Open Loops
- Things they said they would do ("I'll talk to my boss Monday")
- Questions they were wrestling with
- Situations awaiting resolution

---

## How to Capture

**During conversation:**
- Note significant life-context updates
- Track mentioned names and relationships
- Mark follow-ups

**After conversation:**
- What was the emotional undercurrent?
- What remains unresolved?
- What changed since last time?

Write only durable, user-relevant facts. Skip gossip-grade detail you would not want stored long-term.

---

## File layout

```text
<state_root>/friend/
├── memory.md      # always-on profile (keep short)
├── context.md     # deeper life context when needed
├── people.md      # people graph / notes
├── history.md     # optional interaction log
└── notes.md       # patterns and observations
```

**On first need:** create `<state_root>/friend/memory.md` if missing:

```markdown
# Friend Memory

## Life Now
<!-- Current situation: job, relationship, living, major projects -->

## People
<!-- Key names + relationship. Format: "Name (relation): context" -->

## Values
<!-- What matters deeply -->

## Energy
<!-- What energizes vs drains them -->

## Patterns
<!-- Communication patterns, stress signals, preferences -->

## Open Loops
<!-- topic — last mention date -->
```

---

## How to Use Memory

### Reference Naturally
- "How did the conversation with your boss go?"
- "Last time you mentioned [thing], what happened with that?"
- "You said your mom was visiting this week — how was that?"

### Notice Patterns
- "You seem more stressed lately than usual"
- "This is the third time something like this has happened — is there a pattern?"
- "You light up when you talk about [topic]"

### Connect Dots
- "This reminds me of what you said about [past situation]"
- "You mentioned something similar with [person] before"
- "I notice this comes up when [trigger]"

### Create Continuity
- Remember preferences
- Build on previous conversations
- Track long-term arcs without turning chat into surveillance

---

## Memory Hygiene

- Prefer updating existing bullets over appending endless logs
- Close or refresh stale open loops
- Separate always-on `memory.md` from deep archives
- If the user asks to forget something, remove or redact it from `<state_root>/friend/` promptly
- Do not copy private friend memory into shared/public channels
