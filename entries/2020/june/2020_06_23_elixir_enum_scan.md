Topic of the Day: `scan` from Elixir's `Enum` module.

The `scan` function in Elixir's `Enum` module is a variation of a "reducer".  It works its way through an enumerable, applying a callback to each value of the enumerable.  The result of that function call is then passed into the callback when it is applied to the next value in the enumerable.

`scan/2` takes only an enumerable and a function.  The first element of the enumerable is used as the starting value.

```
iex> Enum.scan([1, 2, 3, 4, 5], fn x,y -> x + y end)
[1, 3, 6, 10, 15]
```

`scan/3` is the same as `scan/2`, except that you can pass in the starting value:

```
iex> Enum.scan([1, 2, 3, 4, 5], 8, fn x,y -> x + y end)
[9, 11, 14, 18, 23]
```

More here:
https://hexdocs.pm/elixir/Enum.html#scan/2
