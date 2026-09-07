# Darwin Evaluation Record

## Method

This is a dry-run structural evaluation against the repository's Darwin 9-dimension rubric. The three scenarios in `test-prompts.json` were walked through against `SKILL.md` and the routed references; this record does not claim live clinical diagnosis or real-user execution.

## Score: 85/100

| Dimension | Score | Evidence |
|---|---:|---|
| Frontmatter quality | 7/7 | Name matches the package; description names both supported triggers and excluded diagnosis/prescribing scope. |
| Workflow clarity | 10/12 | `Core Workflow` gives a six-step path from triage to handoff. |
| Failure mode encoding | 10/12 | `Decision Outputs` handles emergency, prompt-review, no-red-flag, and insufficient-photo branches. |
| Checkpoint design | 4/6 | Consent gates persistent writes and exports; urgency is checked before data collection. |
| Executable specificity | 15/18 | State-root precedence, case tree, reference routing, and image-comparison conditions are concrete. |
| Resource integration | 4/4 | Each conditional resource is routed directly from `SKILL.md`. |
| Overall architecture | 10/12 | The concise entry point retains details in directly-routed references. |
| Measured performance | 19/23 | Three dry-run scenarios cover routine tracking, a changing/bleeding lesion, and emergency paediatric rash symptoms. |
| Counter-examples and blacklists | 6/6 | Scope, sensitive-image routing, and common failure modes block diagnosis and unsafe image collection. |
| **Total** | **85/100** | Meets the repository threshold of 80/100. |

## Scenario Results

1. **Routine rash tracking:** triage precedes consented case creation; the record separates symptoms, exposures, and treatment response.
2. **Bleeding, evolving mole:** the workflow recommends prompt in-person evaluation instead of diagnosing from a photo.
3. **Child with systemic rash symptoms:** the emergency path takes precedence over collection, comparison, or storage.

## Limits

The score is a dry-run structural assessment. It should not be treated as clinical validation, a diagnostic accuracy measurement, or evidence that the skill has been tested on real patient data.
