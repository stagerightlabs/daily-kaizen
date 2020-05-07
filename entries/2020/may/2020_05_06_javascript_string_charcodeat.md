Topic of the Day:  Javascript's `String.prototype.charCodeAt()`

`charCodeAt` is a lookup method on the String prototype.  Given an index it will return a character code for the content of the string at that index.

```
const example = "Hello World!"
example.charCodeAt(1)

// Result
// 101 (aka "e")
```

The indexing is zero based. The character at index zero in this example is "H".

The character codes come from UTF-16, an encoding scheme. UTF-16 can be quite complicated; a whole topic unto itself, but most common english language characters in that system are represented by their ASCII codes: http://www.asciitable.com/

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charCodeAt
https://en.wikipedia.org/wiki/UTF-16
