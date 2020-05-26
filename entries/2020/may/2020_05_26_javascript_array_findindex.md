Topic of the Day: Javascript's `Array.prototype.findIndex()`

This method will help you find the index of an item in an array.  Pass it a function and it will return the index of the first array member that evaluates true when run through that function.

For example:

```
const arr = ["red", "orange", "yellow", "green", "blue", "indigo", "violet"]

let index = arr.findIndex(color => color == "green")
// 3
```

If the value you are looking for is not found, it will return -1.

```
const arr = ["red", "orange", "yellow", "green", "blue", "indigo", "violet"]

let index = arr.findIndex(color => color == "hot pink")
// -1
```

I tend to use this quite often when I need to manipulate the contents of an array.  Use `findIndex` to determine where a value is in the array and then use `slice` to remove it or insert addtional values at that location - it can be quite helpful.

The callback will be provided three values, if you need them:

```
let index = arr.findIndex((element, index, array) => {
    // do something
})
```

This is helpful if you need more sophisticated logic in your lookup function.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex
