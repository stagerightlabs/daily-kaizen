Topic of the Day: Javascript's `Object.isFrozen()`

In Javascript a "frozen" object cannot be modified. Existing properties cannot be changed and new properties cannot be added.  The `isFrozen()` method is a helper that lets us determine if an object has been frozen. However, this is really only useful when operating in "strict" mode.

For Example:

```
const chr = {
    name: "Hiro Protagonist",
    occupation: "The Deliverator",
}

Object.freeze(chr)

chr.occupation = "Ex-Deliverator";
// Throws an error (when in strict mode)

chr.location = "The Black Sun"
// Throws an error (when in strict mode)
```

Freezing objects and arrays turns out to be more complicated than one might expect, though we will save the details for another day.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/freeze
