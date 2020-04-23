Topic of the Day: `concat` from Elixir's `Enum` module.

`concat/1` will take an enumerable and "flatten" any enumerables within it by one level:

For example:

```
iex> Enum.concat([ ["a", "b", "c"], ["d", "e", ["f"]] ])
["a", "b", "c", "d", "e", ["f"]]

```

If any of the top level elements are not enumerables an error will be thrown:

```
iex> Enum.concat(["a", "b", "c", "d", "e", ["f"]])
** (Protocol.UndefinedError) protocol Enumerable not implemented for "a"
```

Like many of the functions in the `Enum` module, it will always return a list.

`concat/2` will combine both of the enumerables you provide into a new list:

```
iex> Enum.concat(["a", "b", "c"], ["d", "e", "f"])
["a", "b", "c", "d", "e", "f"]
```

More here:
https://hexdocs.pm/elixir/Enum.html#concat/1
