
The `Object.values()` function was introduced in ES6 to provide an easy way to retrieve all of the property values in an object as an array.  `Object.*` is a global that provides a handful of helper functions that can be used on any object without having to rely on whatever may be available in that objects prototype. (It is technically a function but that is not relevant here.)

For example:

```javascript
var obj = {
    name: "Hiro Protagonist",
    title: "The Deliverator",
}

var arr = Object.values(obj);

// Result:
["Hiro Protagonist", "The Deliverator"]
```

It is important to recognize that this method is not part of the object prototype, so this will not work:

```javascript
var arr = obj.values();

// Result:
// TypeError: obj.values is not a function
```

`Object.values()` also ignores any prototypal values that may exist on the object and only returns data for the keys that belong to the object directly.

Read more: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/values
