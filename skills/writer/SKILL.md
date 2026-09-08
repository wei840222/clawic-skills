---
name: writer
description: Improve drafted prose by diagnosing robotic AI writing patterns and revising for concrete, natural, audience-appropriate writing. Use when drafting, rewriting, editing, or reviewing emails, articles, reports, product copy, or summaries for clearer human-sounding prose.
metadata:
  version: "1.0.2"
  openclaw: '{"emoji":"✍️"}'
---

# Writer

Improve a draft without changing its intended facts, audience, or decision. First identify the few patterns that make the text sound generic; then revise and verify the result.

## Workflow

1. Identify the audience, purpose, and non-negotiable facts. If any are missing, preserve the draft's stated intent and avoid inventing details.
2. Read `references/writing-traps.md` before editing. Use its checks to find only the patterns present in the draft.
3. Revise with concrete subjects and verbs, varied sentence rhythm, and connected prose where relationships matter. Keep terminology consistent with the audience.
4. Compare the revision with the draft. Preserve claims, numbers, commitments, and the requested format; flag any claim that cannot be substantiated rather than fabricating precision.
5. Return the revised text followed by a short note naming the material improvements when the user asked for an explanation or review.

## Boundaries

- Preserve the author's voice when it is identifiable; improve clarity and rhythm rather than replacing it with a house style.
- Keep factual claims supported by the supplied material. Mark unsupported superlatives, metrics, and causal claims for confirmation.
- Retain useful lists for procedures, options, and scannable requirements. Turn a list into prose only when the relationships between ideas need explanation.
- Match the requested level of formality and regional spelling unless the user asks for a different style.

## References

- Read `references/writing-traps.md` for diagnostic checks, revision techniques, examples, and a final self-review pass.
