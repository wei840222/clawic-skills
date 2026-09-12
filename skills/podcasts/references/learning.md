# Learning Mode

## Knowledge Extraction

For educational podcasts, extract:

- Key concepts and frameworks
- Mental models mentioned
- Action items and exercises
- Book / resource recommendations
- Research studies cited (title + enough identity to look up)

Store durable notes in `<state_root>/knowledge.md` (or topic files under `<state_root>/` if the corpus grows).

## Note Structure

Organize by topic, not only by episode:

```text
## Topic: [e.g., Sleep Optimization]

### Sources
- Huberman Lab #42
- Lex Fridman #287
- DOAC with Matthew Walker

### Key Insights
- Insight 1 (source, timestamp when known)
- Insight 2 (source, timestamp when known)

### Action Items
- [ ] Practical step
- [ ] Habit to implement

### Conflicting Advice
- Expert A says X
- Expert B says Y
```

Preserve disagreements instead of collapsing them into a false consensus.

## Spaced Resurfacing

Resurface insights over time when the user wants retention support:

- Day 1: Extract and save
- Day 3: Brief reminder
- Day 7: Short quiz or summary
- Day 30: Connect to newer learnings

This is lightweight review scaffolding, not a clinical spaced-repetition product claim.

## Application Tracking

Track what the user actually applies:

```text
## Applied Insights
| Insight | Source | Applied Date | Result |
|---------|--------|--------------|--------|
| Morning sunlight | Huberman | 2026-01-15 | Better sleep |
```

Only log results the user reports. Do not invent outcomes.

## Cross-Reference Features

- Link related concepts across shows
- Detect when experts disagree
- Surface patterns ("three guests recommend X") when evidence exists
- Keep maps lightweight; prefer markdown links over heavy graph tooling unless requested

## Search Capabilities

Support natural-language lookup over saved notes:

- "What did Huberman say about caffeine?"
- "Negotiation tactics I've learned"
- "Everything from Naval Ravikant"

Prefer semantic search over the user's local notes when available; otherwise keyword search with honest limits.

## Guardrails

- Attribute claims to speakers and episodes; do not upgrade podcast talk to settled science
- Health, legal, and finance takeaways stay informational — point to qualified professionals when stakes are high
- Cite timestamps or section markers when quoting
- Keep all learning state under the resolved `<state_root>`
