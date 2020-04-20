Topic of the Day: Javascript Template Strings

Template strings (or Template Literals) were introduced in ES6 as a means for allowing string interpolation in Javascript. Unlike regular strings, which can use either single or double quotes, template literals are surrounded by backticks:

For Example:

```
var example = `This is a template literal.`;
```

If we have another value we want to interpolate into the string at evaluation time, we can reference that value like this:

```
var name = 'javascript';
var example = `This is a ${name} template literal`;

// Value:
// " This is a javascript template literal";
```

It is also possible to customize how the interpolation is processed for each string by creating "tagged templates" but that is a bit beyond our scope.

Note: This will only work in your browser if it supports ES6 syntax natively.  If not, you will need to use a build tool to convert your code into "plain" javascript before it can be run in your browser.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals
