Topic of the Day: `find_value` from Elixir's Enum module

The `find_value/2` method does two things: it searches for a value in an enumerable and then returns the result of a clojure applied to that value.

Given an enumerable and an anonymous function, it will evaluate the function against each value in the enumerable and return the first resulting value that is truthy.

For example:

```
iex> Enum.find_value(["a","b","c","d"], fn c ->
...>     if c == "c", do: c <> " has been found"
...> end)
"c has been found"
```

"c" is the only value in that list that the anonymous function evaluates as true.   `find_value` then returns the value computed by that anonymous function.

`find_value/3` is similar, but it also accepts a default value that will be returned if no other qualifying value can be found in the enumerable.

```
iex> Enum.find_value([2,4,6,8], "nada" fn c ->
...>     if c > 10, do: c * 10
...> end)
"nada"
```

More here:
https://hexdocs.pm/elixir/1.10.3/Enum.html#find_value/3
