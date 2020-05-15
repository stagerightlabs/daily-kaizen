Topic of the Day: Javascript's `String.prototype.repeat()`

We had a small preview of this yesterday.  The `repeat` method does exactly what it sounds like.  Given an integer it will return a string that contains the first string repeated that many times.

For example:

```
var str = "abc"

str.repeat(3)
// "abcabcabc"

str.repeat(-1)
// RangeError
```

Not much complexity to this one.   More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/repeat
