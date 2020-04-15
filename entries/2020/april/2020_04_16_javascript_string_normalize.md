Topic of the Day: Javascript's `String.prototype.normalize()`

`normalize()` is a method available on the `String` prototype. It will return a string that has converted any unicode code points to their character equivalent. Code points are hex values denoted with a "\u" prefix; their character representations are defined in the unicode standard (https://home.unicode.org/).

For example:

```
var name = "\u0041\u00EF\u0064\u0061";

name.normalize()

// Result:
// "Aïda"

```

`normalize()` can be useful for string manipulation in some cases, but it is most useful when performing string comparison. Some unicode characters can be represented as a composition of two different unicode characters. From a reader's perspective both of these would look identical.

```
var single = "\u00E9" // é
var double = "\u0065\u0301" // e +  ́
```

However, if we compare them, Javascript does not consider them to be the same.

```
single == double

// Result
// false
```

However, if we compare their normalized versions the result matches our expectations:

```
single.normalize() == double.normalize()

// Result
// true
```

More here:

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/normalize
