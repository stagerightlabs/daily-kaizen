Topic of the Day: Javascript's `Object.fromEntries()`

The `fromEntries()` method transforms an array of key/value pairs into an object.

For example:

```
const arr = [
    ['name', 'Hiro Protagonist'],
    ['title', 'The Deliverator'],
]

const obj = Object.fromEntries(arr)

console.log(obj)
// Object {
//    name: "Hiro Protagonist',
//    title: "The Deliverator",
// }
```

The provided value does not have to be an array; it can be any data type that implements the "iterable" protocol; sometimes just called an "iterable".

This method is the opposite of `Object.entries()`, which returns a list of key value pairs from an object.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/fromEntries
