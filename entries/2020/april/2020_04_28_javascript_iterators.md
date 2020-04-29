Topic of the Day: Iterators in Javascript

Iterators are relatively new to Javascript but they have been around in other languages for a long time.

The idea of iterating over a set of data is not new. We can use a `for` loop to cycle through each entry in an array. Similarly, `map`, `filter` and numerous other methods do essentially the same thing; they traverse an array and perform actions on the members of that array.

What happens if we want to iterate over a complex data object with nested structures?  Using a `for` loop in that situation is much less straight forward; what exactly are we looping over?

Imagine a data structure like this:

```
const library = {
    books: [
        {
            title: "Snow Crash",
            author: "Neal Stephenson",
        },
        {
            title: "The Diamond Age",
            author: "Neal Stephenson",
        },
        {
            title: "Neuromancer",
            author: "Bruce Sterling",
        }
    ],
    meta: {
        // Some other information here
    }
}
```

We could iterate over all of the books in this library object by looping over the `library.books` array, or we could turn the library object itself into an "iterable"; something that can be iterated over.  To do that we implement a function on the object with a special name (`[Symbol.iterator]`) and set it up to return an iterator.

```
const library = {
    // ...
    [Symbol.iterator]() {
        let index = 0;
        let books = this.books

        return {
            next() {
                if (index < books.length) {
                    return {value: books[index++].title, done: false}
                } else {
                    return { value: undefined, done: true }
                }
            }
        }
    }
}
```

To be an iterator, all you need is a `next()` function that returns an object with two keys: `value`, representing the next value and `done`, a boolean that tells us whether or not this value is the last value in the sequence.  From there, you have two options for using your iterator:

```
// Manual iteration
var it = library[Symbol.iterator]();

it.next()
// Object { value: "Snow Crash", done: false }
it.next()
// Object { value: "The Diamond Age", done: false }
it.next()
// Object { value: "Neuromancer", done: false }
it.next()
// Object { value: undefined, done: true }
```

```
// Loop iteration
for (book of library) {
  console.log(book)
}

// Snow Crash
// The Diamond Age
// Neuromancer
```

More here:
https://codeburst.io/a-simple-guide-to-es6-iterators-in-javascript-with-examples-189d052c3d8e
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators
