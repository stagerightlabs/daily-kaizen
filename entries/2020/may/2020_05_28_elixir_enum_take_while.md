Topic of the Day: `take_while/2` from Elixir's Enum module.

Given an enumerable collection and a function, `take_while/2` will return all of the member elements until the function returns false. The values returned will always be in a list.

For example:

```
iex> Enum.take_while(["a", "b", "c", "d"], fn ch -> ch != "c" end)
["a", "b"]

iex> Enum.take_while([10, 15, 20, 25], fn x -> x < 20 end)
[10, 15]
```

More here:
https://hexdocs.pm/elixir/Enum.html#take_while/2
