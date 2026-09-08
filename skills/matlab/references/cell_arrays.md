# Cell arrays, strings, and character vectors

Use a numeric or homogeneous array when elements share type and shape. Use a cell array for mixed types or differently sized values:

- `C(1)` returns a 1-by-1 cell array.
- `C{1}` extracts the cell's contents.
- `C{:}` expands contents as a comma-separated list, which is useful only when the receiving function expects separate arguments.

`"text"` creates a string scalar or array; `'text'` creates a character vector. Keep one representation through an operation and convert explicitly at boundaries with `string` or `char`.
