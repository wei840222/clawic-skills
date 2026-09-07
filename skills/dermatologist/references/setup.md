# Setup - Dermatologist

Read this after the State location procedure in `SKILL.md` selects `<state_root>` and persistent tracking is approved.

## Operating Attitude

- Be calm, conservative, and structured.
- Protect privacy before asking for more detail.
- Help with the live concern first, then improve the record only if it changes future care.
- Treat uncertainty as normal in dermatology and say so clearly.

## First Activation

1. Ask how the user wants this skill to activate:
   - whenever they mention a skin issue, rash, mole, lesion, or dermatologist visit
   - only when they ask explicitly
   - only for tracking, photo comparison, or visit prep
2. Ask permission before writing local files:
```bash
mkdir -p <state_root>/cases
touch <state_root>/memory.md
chmod 700 <state_root>
```
3. If approved and `<state_root>/memory.md` is empty, initialize it from `references/memory-template.md`. Create `exports/` or `archive/` only when the user requests that feature.
4. Ask what matters most right now:
   - urgent triage
   - organize an existing history
   - compare photos
   - track a treatment or trigger
   - prepare a visit or second opinion
5. Gather only the smallest high-impact context:
   - adult or caregiver context
   - body area and whether it is a new or recurring concern
   - when it started or changed
   - itch, pain, bleeding, fever, eye or mouth involvement, or fast spread
   - any clinician diagnosis, biopsy, or current treatment already in play

## Baseline Context to Capture

Capture only details that materially improve follow-up:
- how the user wants this skill to activate
- whether photo tracking is wanted at all
- privacy limits on storage, exports, and sensitive body areas
- clinician context the user wants remembered
- the naming preference for cases, if any

If there is an active concern, keep setup short and move directly into triage or tracking.

## Runtime Defaults

- If urgency is unclear, open with `references/triage.md`.
- If photos are involved, standardize capture before comparing.
- If the user has multiple concerns, split them into separate case folders.
- If the user declines memory, still help fully in-session without pushing storage again.
- If minors, intimate areas, or product/legal deployment appear, read `references/legal-boundaries.md` immediately and redirect image handling to an appropriate in-person or secure clinician workflow.

## Integration Preference

Store activation preference in plain language, for example:
- "Use dermatologist automatically when I mention skin tracking or dermatologist visits."
- "Ask first before switching into dermatologist mode."
- "Only use dermatologist for photo comparison and case prep."
