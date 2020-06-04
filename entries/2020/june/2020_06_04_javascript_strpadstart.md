Topic of the Day: Javascript's `String.prototype.padStart()`

`padStart` will add content to the beginning of a string until it reaches a desired length.  If the string is already longer than the desired length nothing will be changed.  The first parameter is the target length, and the second is an optional string you want to use for padding. The default value used for padding is ' '.

For example:

```
const str = "world"

console.log(str.padStart(8))
// "   world"

console.log(str.padStart(12, "hello"))
// "helloheworld"

console.log(str.padStart(3, 'x'))
// "world"
```

Note that the padding string was repeated to fill the extra space. Also note that this method returns a new string and does not modify the original string.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/padStart
