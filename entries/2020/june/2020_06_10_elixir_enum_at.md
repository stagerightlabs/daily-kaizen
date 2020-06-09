Topic of the Day: `at/3` from Elixir's `Enum` module.

Given an enumerable and an index, the `at/3` method will return the value that is found at that index.

For example:

```
iex> Enum.at(["a", "b", "c", "d", "e"], 3)
// "d"
```

You can also optionally specify a default value that should be returned if the index lookup fails.

```
iex> Enum.at(["a", "b", "c", "d", "e"], 10, "x")
// "x"
```

If no default is provided, `at/3` will return `nil` if nothing can be found.

```
iex> Enum.at(["a", "b", "c", "d", "e"], 10)
// nil
```

More here:
https://hexdocs.pm/elixir/1.10.3/Enum.html#at/3
