
`take/2` from Elixir's `Enum` module.

The [`Enum`](https://hexdocs.pm/elixir/Enum.html) module provides a set of functions that can be used with any Elixir data type that is enumerable: `List`, `Map`, `MapSet`, `Range`, and others.

`take/2` returns a `List` of N elements from an enumerable, either from the beginning or the end of the set depending on the amount requested.

For example:

```
iex> Enum.take(["John Hackworth", "Gwendolyn Hackworth", "Fiona Hackworth"], 1)
["John Hackworth"]

iex> Enum.take(["John Hackworth", "Gwendolyn Hackworth", "Fiona Hackworth"], -1)
["Fiona Hackworth"]

iex> Enum.take(["John Hackworth", "Gwendolyn Hackworth", "Fiona Hackworth"], 0)
[]
```

The "/2" in "take/2" refers to the number of parameters the function accepts. (More about that some other time.)

Remember that values in Elixir are immutable, so when using the `take/2` method the original enumerable is not affected, and the result is a brand new value stored separately in memory.

More here:

https://hexdocs.pm/elixir/Enum.html#take/2
