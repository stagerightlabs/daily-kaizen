Topic of the Day: Javascript's `String.prototype.trim()`

There are many scenarios where you might find yourself with a string that contains white space padding.  The `trim()` method will return a new string that has leading and trailing whitespace removed.

For example:

```
let title = '   Snow Crash   '

title.trim()

// 'Snow Crash'

title

// '   Snow Crash   '
```

This function will remove both tabs and spaces.  Note that it returns a new string and does not alter the original string in memory.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/Trim
