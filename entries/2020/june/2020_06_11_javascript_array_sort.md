Topic of the Day: Javascript's `Array.prototype.sort()`

The sort method re-arranges the contents of an array based on user provided function.  If you don't provide a comparison function it will use ascending string comparison as the default.

For example:

```
let arr = ["e", "d", "c", "b", "a"]
arr.sort()
console.log(arr)
// [ "a", "b", "c", "d", "e" ]
```

Note that it is re-arranging the contents of the array in place, which could potentially create problems for you if you are not aware that it is happening. (Arrays and Objects in Javascript are considered mutable.)

A comparison function will be given two items from the array and must return either `-1`, `0`, or `1`.

- `-1` indicates that the first parameter is "less" than the second
- `0` indicates that both parameters are "equal"
- `1` indicates that the first parameter is "more" than the second.

For example:

```
let arr = ["10", "1", "11", "12", "2", "21"]

arr.sort()
// [ "1", "10", "11", "12", "2", "21" ]

arr.sort((a, b) => parseInt(a) - parseInt(b))
// [ "1", "2", "10", "11", "12", "21" ]
```

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort
