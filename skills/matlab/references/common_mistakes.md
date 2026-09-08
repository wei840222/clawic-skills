# Common MATLAB mistakes

- MATLAB indices begin at 1; use `end` for the last valid index in a dimension.
- Prefer `idx` or `k` for loop counters so `i` and `j` retain their conventional imaginary-unit meaning.
- A semicolon suppresses command-window output; add it deliberately after assignments in scripts and loops.
- Use `==` for equality tests and `=` for assignment.
- Use `clearvars` with explicit names when cleanup is necessary; preserve the variables needed to reproduce a defect.
