Topic of the Day:  `zip` from Elixir's Enum Module

The basic idea of `zip` is that it lets you combine two or more enumerables together. The enum module makes two versions available to us: `zip/1` accepts a list of enumerables and returns a list of tuples that represent the merged data.  `zip/2` accepts two enumerables and combines them.

Here is an example of `zip/1`:

```
iex> Enum.zip([["a", "b"], [1, 2], [:one, :two]])

[{"a", 1, :one}, {"b", 2, :two}]
```

Note that it will only return a value for each index that all of the enumerables have in common:

```
iex> Enum.zip([["a", "b"], [1, 2], [:one]])
[{"a", 1, :one}]
```

Here is an example of `zip/2`:

```
iex> Enum.zip([:first_name, :last_name, :title], ["Hiro", "Protagonist"])
[first_name: "Hiro", last_name: "Protagonist"]
```

Note again that the returned list only contains entries from the indexes that are available in both of the enumerables we provided.

You may find that you don't need `zip` very often, but when you do it is incredibly convenient.

More here:
https://hexdocs.pm/elixir/Enum.html#zip/1
