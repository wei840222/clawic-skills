# Setup — Excel / XLSX

Read this on first use, or when `<state_root>/excel-xlsx/memory.md` is missing, to capture only the preferences that change spreadsheet behavior.

## Attitude

Help someone who works with Excel files. They may be frustrated with date bugs, precision loss, or cross-platform surprises. Show that those pains are understood and will be handled deliberately.

Talk about Excel pitfalls and best practices in plain language. The user cares about correct spreadsheets, not about memory files or config jargon.

## Priority order

### 1. Activation

Confirm when this skill should engage:

- Jump in automatically when the user is working with Excel / `.xlsx` / workbook tasks, or
- Wait until they ask directly

Once they choose, reflect the rule back in one short sentence before saving it.

### 2. Working context

Ask only what changes the workflow:

- What they use Excel for (reports, import/export, analysis, templates)
- Libraries/tools (`openpyxl`, `pandas`, SheetJS, xlsxwriter, manual Excel)
- Platforms (Windows, Mac, Linux, mixed)
- Recurring pain points (dates, encoding, large files, ID corruption)

Start broad, then narrow to the details that affect formulas, types, or delivery.

### 3. Preferences (only if they care)

Capture only stated preferences:

- Date system (`1900` / `1904` / `auto`)
- Date format (`DD/MM/YYYY` / `MM/DD/YYYY` / `YYYY-MM-DD`)
- Numeric IDs (`always_text` / `when_needed`)
- Large-file handling (`suggest_streaming` / `handle_normally`)

## After each preference share

1. Reflect the fact you heard.
2. Connect it to the spreadsheet behavior you will protect.
3. Continue the original task.

## What to store (with consent)

Write only user-approved durable facts to `<state_root>/excel-xlsx/memory.md` using `references/memory-template.md`:

- Activation preference
- Tools/libraries
- Primary platform
- Date / numeric-ID / large-file preferences
- Known pain points

Name every write. Keep credentials and workbook contents out of memory.

## Setup is enough when

You know:

1. When to activate
2. Which tools/platform matter for this user

Additional preferences can accumulate through normal use.
