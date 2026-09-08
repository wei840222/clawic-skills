---
name: screenshots
description: Create App Store and Google Play screenshot sets from raw captures, brand assets, and approved copy. Use when preparing, resizing, localizing, reviewing, or exporting mobile-store screenshots; use a general image-editing workflow for unrelated graphics.
metadata:
  version: "1.0.1"
  openclaw: '{"emoji":"📱"}'
---

## State location

Screenshot project state may exist in `<workspace>/screenshots/`, `<workspace>/memory/screenshots/`, or `~/screenshots/`. Before a state operation, resolve `<state_root>` once: use an explicitly configured path when present; otherwise use the first existing directory in that order. If multiple locations exist, use only the highest-precedence location and tell the user that separate copies exist. If none exists and the user asks to save project state, create `<workspace>/screenshots/`; when `<workspace>` is unavailable, ask for a state root rather than guessing from the current directory. Keep every state operation in the selected `<state_root>`.

## Load the right reference

| Task | Read |
| --- | --- |
| Plan required assets, dimensions, or pre-upload checks | `references/specs.md` |
| Choose a layout, frame, palette, or category treatment | `references/templates.md` |
| Write or place localized marketing copy | `references/text-style.md` |
| Run a project from intake through export or recover from a failed check | `references/workflow.md` |
| Record approval feedback or reuse a prior visual decision | `references/feedback.md` |

## Workflow

1. **Intake.** Confirm target stores, locales, source captures, app icon, brand constraints, and whether the user wants persistent project state. Remove or replace sensitive account, personal, or production data visible in captures before sharing an output.
2. **Plan.** Read `references/specs.md` for the selected store and `references/templates.md` for the category. List the selected device classes and locales before composing. Record the chosen sizes, layout, copy, and frame in `<state_root>/{app-slug}/config.md` only after state saving is requested.
3. **Compose.** Read `references/text-style.md`; build one message per screenshot and adapt overlay placement to each target aspect ratio. Use the source capture at its highest available resolution.
4. **Verify.** Read `references/workflow.md` and complete its visual, file, and store-readiness checks. When a check fails, correct the affected source or layout and regenerate every affected size before presenting it.
5. **Approve and export.** Present previews for approval before final delivery. After approval, preserve the batch as `<state_root>/{app-slug}/v{n}/`, point `latest` to the approved version when symlinks are supported, and package the requested store folders.

## Recovery paths

- If raw captures, brand assets, or target-store details are missing, return an intake checklist and wait for the missing inputs rather than fabricating them.
- If multiple candidate state directories exist, use the highest-precedence one selected in **State location** and report the duplicate copies; keep them separate.
- If a platform preview or upload rejects an asset, read `references/specs.md`, retain the rejection reason, correct that constraint, and rerun the verification step for the full affected set.

## Project state

After `<state_root>` is resolved, create only the state needed for the requested project:

```text
<state_root>/
├── memory.md                  # optional cross-project preferences; create after user requests persistence
└── {app-slug}/                # create for an active project
    ├── config.md              # approved brand and export decisions
    ├── raw/                   # provided source captures
    ├── v{n}/                  # immutable exported batches
    └── latest -> v{n}/        # current approved batch, when supported
```

Read `<state_root>/memory.md` before reusing saved preferences. Keep prior approved batches intact; use a new version directory for each export. `references/` is part of the installed skill, not project state.
