Topic of the Day: Javascript Proxies

Proxies were introduced into Javascript as part of ES6. They provide a way to define "hooks" that can intercept and alter common actions you perform in the language; you could think of it as a form of meta-programming.

A proxy is defined with a "target" and a "handler".  The target is the object that will have its behavior modified. The handler is an object that defines the "traps" that implement modified behavior.  Think of a trap as a function that is executed after a certain behavior is triggered but before it completes, allowing you to intercept and modify the response.

Here is an example of a Proxy definition:

```
const person = {
    name: "Da5id",
    location: "The Black Sun"
}
const handler = {
    get: function(target, property) {
        if (property == 'name') {
            return 'Hiro Protagonist';
        }
    }
}
const p = new Proxy(person, handler);

console.log(p.name)
// 'Hiro Protagonist'

console.log(p.location)
// undefined

console.log(person.name)
// "Da5id"

console.log(person.location)
// "The Black Sun"
```

Note that we only see the modified behavior when we interact with the proxy, not the original object.  In this example we did not define a response for retrieving a value other than "name", so the output of `p.location` is `undefined`.

There are many different types of actions that you can intercept with a proxy - see here for a complete list: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy/handler

Proxies are very powerful but they can lead to unintended behavior if you are not careful. The Vue.js internals have been re-written almost entirely with proxies for the upcoming 3.0 release.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Meta_programming
