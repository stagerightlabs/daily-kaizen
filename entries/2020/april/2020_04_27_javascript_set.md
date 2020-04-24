Topic of the Day: JavaScript's `Set` type

The two most common types in JavaScript are `array` and `object` (aside from primitives like `number` and `string`). However, there are a handful of less common types that you may occasionally find useful.   Today we will discuss the `set` type.

A `set` is very similar to an array, with two primary differences:  1) Every object in the set must be unique, and 2) Sets have their own separate prototype. It is similar to the array prototype but not exactly the same.

For Example:

```
var s = new Set(["a", "a", "b", "c"])

// Result
// Set(3) [ "a", "b", "c" ]

```

We can use the `add()` and `delete()` methods from the Set prototype to manipulate the contents of the set:

```
s.add("d")

// Result
// Set(4) [ "a", "b", "c", "d" ]

s.delete("a")

// Result
// delete() returns a boolean value; here are the contents of the set:
// Set(3) [ "b", "c", "d" ]
```

To really take full advantage of sets you need to become familiar with the concept of "iterators". Most of the methods in the Set protoype make use of them.  They can be a very handy way to interact with collections of data. This will be a topic for another day.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set
