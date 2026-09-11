# Core Rules

### 1. Treat Calendar.app as the Unified Calendar Source
- Assume provider sync already happens inside Calendar.app and operate on that local unified view.
- Limit authentication to local CLI mechanisms; initiate Google, Microsoft, or Apple OAuth only if the user explicitly requests external setup help.

### 2. Detect Command Path Before Any Calendar Action
- Probe available tools in strict order: `apple-calendar-cli`, then `icalBuddy`, then `shortcuts`, then `osascript`.
- If no path is available, pause execution and explain the missing requirement rather than guessing commands.

### 3. Use Deterministic Time Inputs and Calendar Scopes
- Normalize all user time inputs to explicit timezone and start/end boundaries before running commands.
- Confirm date interpretation when input is ambiguous such as "next Friday" or locale specific formats.

### 4. Read First, Then Write, Then Verify
- For create, update, or delete operations, run a bounded pre-read in the target time window.
- After each write, run read-back verification and report final state with title, time, and calendar.

### 5. Confirm Destructive or Broad Changes
- Always require explicit confirmation for delete, move across calendars, and multi-event edits.
- If confidence is low due to duplicate titles, ask a disambiguation question before any write.

### 6. Keep Recurrence and All-Day Semantics Explicit
- Confirm recurrence rule, timezone behavior, and all-day interpretation before writing recurring events.
- Make all defaults explicit to prevent shifting recurring events after DST changes.

### 7. Prioritize Minimal Exposure and Local-First Handling
- Use only the fields required for the requested action.
- Limit data export strictly to the requested time window and details during a narrow lookup.
- Keep all event data completely local to the machine.
