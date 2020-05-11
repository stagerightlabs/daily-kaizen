Topic of the Day: Javascript's `String.prototype.codePointAt()`

The `codePointAt` method returns the unicode code point value for a given index in a string:

For example:

```
var str = "abcdefg"

str.codePointAt(0)
// 97

str.codePointAt(1)
// 98

str.codePointAt(100)
// undefined
```

The return value is an integer that refers to a unicode symbol.  For most common english language characters this will be equivalent to the letter's ascii value.  This number can often be used as an html code that represents the character in question.

```
var shrug = '🤷'

shrug.codePointAt(0)
// 129335
// HTML code: &#129335;
```

https://unicode-table.com/en/ is an excellent resource for looking up unicode values.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/codePointAt
