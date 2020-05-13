Topic of the Day: Javascript's rest operator

You may occasionally find that you want to define a function but you may not know how many arguments it will need until run time, or you may need it to accept a variable number of arguments. This is exactly the scenario that the rest operator was created for.  New as of ES6, the rest operator tells javascript that you want to accept a variable number of parameters in your function.

For example:

```
function concat(...letters) {
    return letters.join('')
}

concat("a", "b", "c", "d")
// "abcd"

concat("h", "i")
// "hi"
```

The rest operator si the three periods that proceed the name of our variable. Our function will then receive that variable as an array containing all the parameters that were passed into the function.

You can also use it to define a function that has a certain number of required parameters and an unlimited number of optional parameters.

```
function concatAndRepeat(n, ...letters) {
    return letters.join('').repeat(n)
}

concatAndRepeat(2, "h", "e", "l", 'l', "o")
// "hellohello"
```

If no additional parameters are specified the provided array will be empty.

```
concatAndRepeat(2)
// ""
```

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters
