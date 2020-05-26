Topic of the Day: Javascript's `Object.seal()`

In Javascript you now have the option of marking an object as "sealed".  This will prevent the ability to add and remove properties from that object in the future, though the values of existing properties can still be changed.

For example:

```
const jph = {
    name: "John Hackworth",
    position: "Nanotech Engineer",
}

Object.seal(jph)

jph.name = "John Percial Hackworth"
jph.phyle = "New Atlantis"
delete jph.position;

console.log(jph)
// {
//   name: "John Percival Hackworth",
//   position: "Nanotech Engineer",
// }
```

You can see that once the object was locked we were not able to add or remove properties, though we were able to update the existing "name" property.

Interestingly, when you attempt to manipulate a sealed object the response you receive will not necessarily inform you that your actions were unsuccessful.  If you are working in "strict" mode you may see a `TypeError` but otherwise there may be no indication.

It is also worth noting that you cannot change the prototype of a sealed object.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/seal
