Topic of the Day: Javascript's `Array.prototype.join()`

The `join()` method on the array prototype combines all of the elements into a single string.

For example:

```
const arr = ['waterhouse', 'lavender', 'rose'];

console.log(arr.join())
// "waterhouse,lavender,rose"
```

You can specify a separator to place inbetween the elements of the array if you would like.  The defauly separator is a comma.

```
console.log(arr.join(''))
// "waterhouselavenderrose"

console.log(arr.join('_'))
// "waterhouse_lavender_rose"
```

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join
