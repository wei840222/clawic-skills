# Matrix and element-wise operations

Use matrix operators when the expression represents linear algebra and operand dimensions satisfy the matrix rule:

- `A * B` performs matrix multiplication; `A .* B` multiplies corresponding elements.
- `A / B` is right matrix division; `A \ B` solves `A * X = B` without explicitly computing `inv(A)`.
- `A ^ n` is matrix power for a square matrix; `A .^ n` raises each element independently.

Before changing an operator, compare `size(A)` and `size(B)`. A dot operator is correct only when the intended result is per-element; it does not repair an incompatible matrix-algebra model.
