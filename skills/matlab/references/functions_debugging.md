# Functions and debugging

Use functions to make inputs and outputs explicit:

```matlab
function y = scaleSignal(x, factor)
    arguments
        x (:,1) double
        factor (1,1) double = 1
    end
    y = factor .* x;
end
```

For releases that support it, an `arguments` block declares expected classes, shapes, and defaults. Otherwise validate inputs with explicit checks and give an actionable error.

To diagnose a failure, run `dbstop if error`, reproduce it, and inspect `whos`, `size`, and the relevant operands in the debugger. Use `dbclear all` after diagnosis to remove temporary breakpoints.
