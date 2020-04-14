
`take/2` from Elixir's `Enum` module.

The [`Enum`](https://hexdocs.pm/elixir/Enum.html) module provides a set of functions that can be used with any Elixir data type that is enumerable: `List`, `Map`, `MapSet`, `Range`, and others.

`take/2` accepts an enumerable and an integer (N) and returns a `List` of N elements from the enumerable, either from the beginning or the end of the set depending on the value of N.

For example:

```
iex> Enum.take(["John Hackworth", "Gwendolyn Hackworth", "Fiona Hackworth"], 1)
["John Hackworth"]

iex> Enum.take(["John Hackworth", "Gwendolyn Hackworth", "Fiona Hackworth"], -1)
["Fiona Hackworth"]

iex> Enum.take(["John Hackworth", "Gwendolyn Hackworth", "Fiona Hackworth"], 0)
[]
```

Remember that values in Elixir are immutable, so when using the `take/2` method the original enumerable is not affected and the result is a brand new value stored separately in memory.

The "/2" in `take/2`1 refers to the number of parameters the function accepts. (More about that some other time.)

IEX is the interactive Elixir shell, which is a REPL similar to the console in your browser. If you [install Elixir](https://elixir-lang.org/install.html) on your system you can use IEX to experiment with Elixir.

More here:

https://hexdocs.pm/elixir/Enum.html#take/2
