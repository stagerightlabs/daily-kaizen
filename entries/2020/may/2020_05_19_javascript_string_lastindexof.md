Topic of the Day: Javascript's `String.prototype.lastIndexOf()`

The `lastIndexOf()` method searches through a string from back to front, looking for a substring provided by the user.  If found, it will return the index of that substring, if not it will return -1.

For Example:

```
const str = "The Deliverator belongs to an elite order, a hallowed subcategory."

str.lastIndexOf("hallowed")
// 44

str.lastIndexOf("diamond")
// -1
```

You can optionally specify an index that you want to start searching from:

```
const str = "Right now he is preparing to carry out his third mission of the night."

str.lastIndexOf("is")
// 50

str.lastIndexOf("is", 49)
// 40
```

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/lastIndexOf
