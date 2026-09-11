# Common Traps

- Editing by title only when duplicates exist -> wrong event modified.
- Writing recurring events without timezone confirmation -> drift after DST.
- Deleting without pre-read snapshot -> difficult recovery.
- Trusting one CLI path blindly -> brittle behavior across macOS setups.
- Running broad searches by default -> noisy output and accidental edits.
