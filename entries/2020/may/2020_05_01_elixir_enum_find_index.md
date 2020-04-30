Topic of the Day: `find_index/2` from Elixir's `Enum` module.

The `find_index/2` function will locate the zero-based index of a value in an enumerable. It accepts an enumerable as its first parameter, and a function as its second parameter.  The function will be run against all of the values in the enumerable; the index of the first value that the callback evaluates as true will be returned.

If no index can be found, the function will return `nil`.

For example:

```
iex> Enum.find_index(["a", "b", "c", "d", "e"], fn c -> c == "c" end)
2
iex> Enum.find_index(["a", "b", "c", "d", "e"], fn c -> c == "z" end)
nil
```

It will only return one index; if there are multiple values in the enumerable that meet the qualifications you are looking for, only the first index will be returned.

More here:
https://hexdocs.pm/elixir/master/Enum.html#find_index/2
