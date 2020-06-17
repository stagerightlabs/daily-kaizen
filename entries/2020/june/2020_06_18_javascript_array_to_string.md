Topic of the Day:  Javascript's `Array.prototype.toString()`

The `toString()` method on the Array prototype returns the array formatted as a string:

```
const arr = [1, 2, 3, 4, 5]

console.log(arr.toString())
// "1,2,3,4,5"
```

Note: you cannot control the way that the array is represented as a string - this method takes no arguments.  If you want more specific control you can use `Array.prototype.join()` instead.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/toString
