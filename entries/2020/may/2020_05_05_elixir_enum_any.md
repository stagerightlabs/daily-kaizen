Topic of the Day:  `any?` from Elixir's Enum module.

The `any?/2` function will return true if a given callback returns true for any member of an enumerable.  This is helpful for determining the general nature of the content of the enumerable.

For example, we could ask: Are there any even numbers in this enumerable?

```
iex> Enum.any?([1, 2, 3], fn n -> rem(n, 2) == 0 end)
true

iex> Enum.any?([1, 3, 5], fn n -> rem(n, 2) == 0 end)
false
```

Or we could ask, does a group of numbers contain a value higher than a certain threshold?

```
iex> Enum.any?([10, 20, 30], fn n -> n > 25 end)
true

iex> Enum.any?([10, 20, 30], fn n -> n > 50 end)
false
```

Note the use of the question mark in the function name. Generally speaking, Elixir uses this to indicate that the function will return a boolean value.  This is just a convention, not a hard and fast rule.

There is also a variant of this method, `any?/1` that does not make use of a second parameter.  This function checks each member of an enumerable for truthiness.  If any values do evaluate as true, `any?/1` will return true.

```
iex> Enum.any?([true, false, false])
true

iex> Enum.any?([false, false, false])
false
```

More here:
https://hexdocs.pm/elixir/Enum.html#any?/2
