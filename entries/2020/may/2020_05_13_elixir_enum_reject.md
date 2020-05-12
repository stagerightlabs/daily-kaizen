Topic of the Day: `reject/2` from Elixir's `Enum` module

The `reject/2` function accepts an enumerable and an anonymous function.  It cycles through all the values in the enumerable and "rejects" the ones that evaluate as true when run through the closure.

For example:

```
iex> Enum.reject(["a", "b", "c", "d"], fn ltr -> ltr == "b" end)
["a", "c", "d"]

iex> Enum.reject([1, 2, 3, 4, 5], fn n -> n > 3 end)
[1, 2, 3]
```

This is the inverse of the "filter/2" method which retains values that evaluate as true.

More here:
https://hexdocs.pm/elixir/Enum.html#reject/2
