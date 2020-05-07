Topic of the Day: Javascript's `Number.prototype.toPrecision()`

`toPrecision()` is a method on the number prototype that lets us present numbers to a specific number of significant digits. It returns a string; it does not change the number itself.

For example:

```
12.3456.toPrecision(3)

// Result
// 12.3

12.3456.toPrecision(8)

// Result
// 12.345600

0.0040.toPrecision(1)

// Result
// 0.004
```

Note that we are not designating a specific number of decimal places, but rather the general precision of the number (aka Sig Figs).

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toPrecision
