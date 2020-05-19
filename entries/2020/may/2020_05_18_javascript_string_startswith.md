Topic of the Day: Javascript's `String.prototype.startsWith()`

The `startsWith()` method on the string prototype accepts a string and returns a boolean.  If the target string starts with the string you provide the result will be `true`, otherwise `false`.

For example:

```
const title = "Snow Crash"

title.startsWith("Snow")
// true

title.startsWith("Diamond")
// false
```

You can optionally provide an index point to start the check:

```
const title = "Snow Crash"

title.startsWith("Snow", 5)
// false

title.startsWith("Crash", 5)
// true
```

Keep in mind that this method performs a case sensitive check.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/startsWith
