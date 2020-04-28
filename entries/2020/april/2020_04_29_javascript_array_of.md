Topic of the Day: Javascript's `Array.of()` method.

The `Array.of` method provides a quick way to generate an array, or convert existing data into an array.

For example:

```
Array.of("a", "b", "c")

// Result
// [ "a", "b", "c" ]
```

You might be tempted to use the array constructor to achieve the same goal, but this doesn't work in the same way.

```
Array(3)

// Result
// [ undefined, undefined, undefined ]
```

This method seems simple but it can be surprisingly useful.  Often when you are working with the DOM you might end up with a `NodeList` representing a set of nodes. Sometimes you may actually want to convert it into an array to manipulate it with array methods:

```
let tree = document.querySelectorAll('.hello')

// Result
// NodeList [ div.hello, div.hello ]

Array.of(...tree).map(div => {
    // do something...
})
```

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/of
