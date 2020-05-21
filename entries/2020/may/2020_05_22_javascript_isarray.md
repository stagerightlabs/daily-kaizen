Topic of the Day: Javascript's `Array.isArray()`

The `isArray` method offers a quick tool for determining if a given value is an array or not.  It returns a boolean.

For example:

```
const obj = {}
const arr = []
const str = 'hello'

Array.isArray(obj) // false
Array.isArray(arr) // true
Array.isArray(str) // false
```

Very simple but very handy!

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray
