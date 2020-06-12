Topic of the Day:  Javascript's `Number.parseInt()`

The `parseInt()` method accepts a string and returns the integer equivalent. This function can be referenced either as `Number.parseInt()` or as just `parseInt()`.

For example:

```
parseInt("256")
// 256
```

You can also optionally provide a second parameter that specifies the base system you want the number interpreted with.

```
parseInt("256", 16)
// 598

parseInt('abc', 16)
// 2748

parseInt('0101010', 2)
// 42
```

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseInt
