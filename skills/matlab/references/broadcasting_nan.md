# Missing values and expansion

`NaN` is not equal to itself, so test missing floating-point values with `isnan`:

```matlab
hasMissing = any(isnan(A), 'all');
```

Most arithmetic propagates `NaN`. For aggregate functions, use the documented missing-data option when omission is intended, for example `sum(A, 'omitnan')` or `mean(A, 'omitnan')`. State that choice because omitting missing values changes the statistic.

For implicit expansion, verify each dimension is equal or one operand has size 1 in that dimension. If neither condition holds, reshape deliberately rather than relying on an accidental transpose.
