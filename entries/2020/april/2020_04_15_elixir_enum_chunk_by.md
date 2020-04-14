
`chunk_by/2` from Elixir's `Enum` module.

`chunk_by/2` accepts two parameters: an enumerable and a function.  It runs the function over each item in the enumarable and splits them into separate groups each time a different value is returned from the closure.

For example:

```
iex> Enum.chunk_by([2, 2, 2, 3, 3, 4, 4, 6, 7, 8], fn n ->
...>    rem(n, 2) == 1
...> end)
[[2, 2, 2], [3, 3], [4, 4, 6], [7], [8]]
```

Here we are using the `rem/2` method to determine if the remainder of each value when divided by two is equal to one, meaning it is an even number.

Anonymous functions in elixir usually take this form:

```
fn a, b ->
    do_something()
end
```

All functions in elixir have "implicit" returns, meaning that you don't need to specifically say "return x" in a function; the value of the last line is automatically considered to be the return value.  In the example above this is a boolean value.

As `chunk_by/2` traverses the enumerable it groups each value into a new list whenever the result of the anonymous function changes.  In our example this means that if it is working with a group of even numbers and it suddenly encounters an odd number it will start a new list grouping.

It is important to note that it is not grouping the entire set into even numbers and odd numbers, it is just "chunking" them whenever a new value is computed.

```
iex> Enum.chunk_by(["a", "b", "c", "a", "d", "e", "f"], fn n ->
...>    n == "a"
...> end)
[["a"], ["b", "c"], ["a"], ["d", "e", "f"]]
```

More here:
https://hexdocs.pm/elixir/Enum.html#chunk_by/2
