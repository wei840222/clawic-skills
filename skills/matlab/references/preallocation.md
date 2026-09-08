# Preallocation and implicit expansion

Allocate an array to its final size before assigning it in a loop:

```matlab
n = 1000;
y = zeros(n, 1);
for k = 1:n
    y(k) = k^2;
end
```

Use `zeros`, `ones`, `nan`, `false`, `strings`, or `cell` with the intended size and type. Preallocation avoids repeated memory allocation and copying.

MATLAB releases R2016b and later support implicit expansion for compatible singleton dimensions, for example `[1; 2; 3] + [10 20]`. For code that must run on older releases, use `bsxfun(@plus, a, b)` or reshape operands explicitly.
