Topic of the Day: Javascript's `Array.prototype.splice()`

Splice is a very handy tool that lets you add and remove elements of an array at any index point.  The first parameter is the index you want to operate at, and the second is the count of how many elements you want to remove.

```
const arr = ["a", "b", "c", "d"]

arr.splice(0, 1)

console.log(arr)
// ["b", "c", "d"]
```

You can provide any number of optional arguments after that and those values will be inserted into the array at the specified index.

```
const arr = ["a", "b", "c", "d"]

arr.splice(0, 1, "x", "y", "z")

console.log(arr)
// ["x", "y", "z", "b", "c", "d"]
```

If you set the deletion count to be zero nothing will be removed:

```
const arr = ["a", "b", "c", "d"]

arr.splice(0, 0, "x", "y", "z")

console.log(arr)
// ["x", "y", "z", "a", "b", "c", "d"]
```

Note that this method returns the array items that were removed, and updates the array itself in memory.

This method is very useful when used in combination with `findIndex`.  These two together make it very easy to find and remove any element from an array.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice
