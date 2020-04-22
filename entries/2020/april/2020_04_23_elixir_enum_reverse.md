Topic of the Day: `reverse/1` and `reverse/2` from Elixir's `Enum` module.

This one is pretty straight forward.  Given an enumerable such as a list or a map, `reverse/1` will generate a new list with the contents in reverse order. Note that this function will always return a list, regardless of the type of enumerable that it receives.

For example:

```
iex> Enum.reverse(["a", "b", "c"])
["c", "b", "a"]

iex> Enum.reverse(%{a: 1, b: 2, c: 3})
[c: 3, b: 2, a: 1]
```

`reverse/2` is similar, though it takes an enumerable as a second parameter that will be appended to the reversed contents of the first enumerable:

```
iex> Enum.reverse(["a", "b", "c"], ["d", "e"])
["c", "b", "a", "d", "e"]

iex> Enum.reverse(%{a: 1, b: 2, c: 3}, %{d: 4, e: 5})
[c: 3, b: 2, a: 1, d: 4, e: 5]
```

More here: https://hexdocs.pm/elixir/Enum.html#reverse/1
