# Indexing

- 1-based indexing — first element is `A(1)`, not `A(0)`
- `end` keyword for last index — `A(end)`, `A(end-1)`, works in any dimension
- Linear indexing on matrices — `A(5)` accesses 5th element column-major order
- Logical indexing returns vector — `A(A > 0)` gives 1D result regardless of A's shape
