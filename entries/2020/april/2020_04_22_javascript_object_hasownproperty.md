Topic of the Day: Javascript's `Object.prototype.hasOwnProperty()`

Unlike Ruby, PHP or most other object oriented languages, Javascript makes use of "Prototypal" inheritance rather than class based inheritance.  When you create an object in Javascript it automatically receives a set of functionality from a previously defined "prototype".  If you log the object in your browser console you can inspect the contents of the prototype.  A method or property defined in the prototype can be called on the object directly:

For example:

```
var obj = {foo: "bar"}
obj.toString()

// Result
// "[object Object]"
```

All objects inherit the same prototype, but each individual object might have different properties and functions contained within them. If you really want to, you can modify that prototype and add your own properties and methods.  This is generally considered a bad practice, but it is possible.  This means that we can never really be sure what might be in an object's prototype.

Usually this is not a problem but there are times when we want to know if an object has a certain item or value within it. We could try to reference the item directly; if it doesn't exist in the object it will return "undefined".  However, what if that item is defined in the object's prototype?  We will get the prototype value returned to us instead. This makes checking the contents of an object a somewhat unreliable business.

```
var obj = {foo: "bar"}

obj.baz

// Result
// undefined


obj.toString

// Result
// function toString()
```

To get around this we can use the `hasOwnProperty()` method, which itself comes from the object prototype. This method will check to see if a certain key is set on the object itself, and it will ignore the contents of the object's prototype.

```
var obj = {foo: "bar"}

obj.hasOwnProperty('baz')

// Result
// false

obj.hasOwnProperty('foo')

// Result
// true

obj.hasOwnProperty('toString')

// Result
// false
```

There is one important thing to keep in mind. `hasOwnProperty` will return true if the requested key exists even if that key represents a falsey value.

```
var obj = {baz: false}

obj.baz

// Result
// false

obj.hasOwnProperty('baz')

// Result
// true

```

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty
