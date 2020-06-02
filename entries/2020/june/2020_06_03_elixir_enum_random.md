Topic of the Day: `random/1` from the Elixir `Enum` module.

The `random/1` method from the Enum module returns a random element from an enumerable.

For example:

```
iex> Enum.random(["a", "b", "c", "d"])
"d"
```

If you pass in a range it will return a random value from within the bounds of the range; it does this in constant time without traversing the entire range.

```
iex> Enum.random(1..10)
9
```

More here:
https://hexdocs.pm/elixir/Enum.html#random/1
