Topic of the Day: Javascript's `Number.isFinite()`

The `isFinite` method offers a quick way to determine if you are working with a value that can be used for finite calculations. This usually refers to whole integers or floating point numbers that have a know length of decimals. Irrational numbers or non numerical values and limits don't count.

For example:

```
console.log(Number.isFinite(1))
// True

console.log(Number.isFinite(Infinity))
// False

console.log(Number.isFinite(NaN))
// False
```

I think it is safe to say that you will most commonly be using finite numbers for most of the math you may need to do on a day to day basis, but for the occasional times when things get a bit more complex this can be helpful.

More here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/isFinite
