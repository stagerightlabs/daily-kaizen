Topic of the Day: `unshift()` from Javascript's array prototype.

If you have an array of values in Javascript you may occasionally want to add a new value to the beginning of the list.  To do that we can use the `unshift()` method from the array prototype:

For example:

```
let arr = ["b", "c"];

arr.unshift("a");

// Result:
// arr now equals ["a", "b", "c"]
```

The `unshift()` method returns the length of the new list. The existing value of `arr` has been changed for us because Arrays and Objects are mutable in Javascript, by design.

Why is this method called "unshift"?  Because the method for removing an item from the beginning of an array is called "shift", and we are doing the opposite.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift
