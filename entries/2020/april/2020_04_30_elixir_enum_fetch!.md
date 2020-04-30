Topic of the day: `fetch/2` from Elixir's `Enum` module.

`fetch/2` retrieves an item from an enumerable at a given index. It requires two parameters: An enumerable and a numerical index.

For example:

```
iex> Enum.fetch(["a", "b", "c", "d"], 2)
{:ok, "c"}
```

There are two important things to take note of here: 1) The index value is zero based, meaning that "a" is at index zero, "b" is at index 1 and so on.  2) The return value is a tuple containing a status atom and the value itself.

What would happen if we requested an index that does not exist?

```
iex> Enum.fetch(["a", "b", "c", "d"], 8)
:error
```

There are times when you might find it useful to throw an exception if you attempt to access an index that does not exist. For those scenarios you can use `fetch!/2`. The exclamation point is often used in Elixir to indicate that a function will raise an error if it does not succeed.

```
iex> Enum.fetch!(["a", "b", "c", "d"], 2)
"c"
iex> Enum.fetch!(["a", "b", "c", "d"], 8)
** (Enum.OutOfBoundsError) out of bounds error
    (elixir 1.10.3) lib/enum.ex:881: Enum.fetch!/2
```

Note that the successful response did not return a tuple, just the value itself.

More here:
https://hexdocs.pm/elixir/Enum.html#fetch/2
