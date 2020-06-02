Topic of the Day: Javascript's `Array.prototype.lastIndexOf()`

The `lastIndexOf` method on the Array prototype is very similar to the `lastIndexOf` method on the String prototype. It returns the last index of a value within an array, using "strict" comparison to determine equality.

For example:

```
const letters = ["a", "b", "c", "a", "b", "c"]

console.log(letters.lastIndexOf("a"))
// 3
```

If the value is not found it will return -1.

```
console.log(letters.lastIndexOf("d"))
// -1
```

You can also specify an index to start the search at. Keep in mind that the method will search through the array from back to front, regardless of where it starts:

```
console.log(letters.lastIndexOf("a", 2))
// 0
```

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/lastIndexOf
