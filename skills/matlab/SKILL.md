---
name: matlab
description: Resolve common MATLAB mistakes involving indexing, matrix versus element-wise operations, vector shapes, preallocation, NaN values, cell arrays, functions, and debugging. Use when writing or fixing MATLAB code with array dimensions or vectorization issues.
metadata:
  version: "1.0.0"
  openclaw: '{"emoji":"📐","requires":{"bins":["matlab"]}}'
---

## MATLAB troubleshooting workflow

1. Identify the expression's operand sizes with `size`, and decide whether the operation is matrix algebra or element-wise.
2. Reproduce the smallest failing expression. For numerical anomalies, inspect values with `isnan`, `isinf`, and `whos` before changing the algorithm.
3. Apply the narrow correction, then state the expected output shape and MATLAB release assumptions.
4. For loops that build arrays, preallocate the final size. When the final size is unknown, collect data with an appropriate container and convert once.
5. If the failure remains opaque, use `dbstop if error` and inspect the stopped workspace; avoid `clear` while diagnosing because it destroys evidence.

Load the smallest reference needed for the current issue:

| Topic | Reference | Load when |
| --- | --- | --- |
| Indexing and dimensions | [references/indexing.md](references/indexing.md) | Resolving indices, linear indexing, logical indexing, or row/column shape mismatches. |
| Operators | [references/matrix_ops.md](references/matrix_ops.md) | Choosing matrix versus element-wise arithmetic or solving linear systems. |
| Allocation and expansion | [references/preallocation.md](references/preallocation.md) | Optimizing loops, sizing arrays, or supporting pre-R2016b code. |
| Missing values | [references/broadcasting_nan.md](references/broadcasting_nan.md) | Handling implicit expansion, `NaN`, or omitted missing values. |
| Containers and text | [references/cell_arrays.md](references/cell_arrays.md) | Selecting cell indexing, strings, or character vectors. |
| Functions and debugging | [references/functions_debugging.md](references/functions_debugging.md) | Defining functions, validating inputs, or using the debugger. |
| Source notes | [references/source-notes.md](references/source-notes.md) | Confirming MathWorks documentation and release-sensitive behavior. |

## Output expectations

Give the corrected MATLAB snippet first. Then explain the operator or shape rule that caused the issue, name any version constraint, and include one quick check such as `size(result)` or an assertion when it reduces recurrence.
