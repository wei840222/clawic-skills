# Memory Template — Excel / XLSX

Create `<state_root>/excel-xlsx/memory.md` with this structure:

```markdown
# Excel / XLSX Memory

## Status
status: ongoing
last: YYYY-MM-DD
integration: pending | done | declined

## Environment
platform: windows | mac | linux | mixed
libraries: [openpyxl, pandas, xlsxwriter, SheetJS, etc.]

## Preferences
date_system: 1900 | 1904 | auto
date_format: DD/MM/YYYY | MM/DD/YYYY | YYYY-MM-DD | none
numeric_ids: always_text | when_needed | none
large_files: suggest_streaming | handle_normally

## Pain Points
<!-- Things they've mentioned struggling with -->
- [e.g., "dates always break when opening on Mac"]
- [e.g., "phone numbers lose leading zeros"]

## Common Tasks
<!-- What they typically do with Excel -->
- [e.g., "export reports for finance team"]
- [e.g., "import CSVs from legacy system"]

## Notes
<!-- Other observations -->

---
*Updated: YYYY-MM-DD*
```

## Status values

| Value | Meaning | Behavior |
| --- | --- | --- |
| `ongoing` | Still learning | Gather context while working |
| `complete` | Has enough context | Work with stored defaults |
| `paused` | User said "not now" | Work with the information already available |

## Preference defaults

If no preference is specified:

- **date_system:** `auto` (detect from workbook)
- **date_format:** ISO (`YYYY-MM-DD`) when generating; preserve when reading
- **numeric_ids:** `when_needed` (warn for >15 digits or leading zeros)
- **large_files:** `suggest_streaming` (mention for 100K+ rows)

## What to track over time

- Which warnings helped versus annoyed them
- Libraries they actually use
- Recurring issues worth promoting into pain points
- Explicit preference changes

## Integration note

After the user confirms preferences, store activation timing and the key spreadsheet defaults only under `<state_root>/excel-xlsx/`.
