Topic of the Day: `slice/2` and `slice/3` from Elixir's Enum module

The slice function is very similar to the array slice method in Javascript.  Given an enumerable it will return a list of elements from that enumerable based on your specifications.   There are two versions of slice in Elixir's Enum module:

`slice/2` accepts an enum and a range and returns the list of elements at the indexes specified by the range. In elixir a "range" is a shorthand method for listing a series of sequential values, using the ".." operator.  The range of numbers from one to ten could be represented like this:  `1..10`.  It is also possible to use ranges with characters but there are additional steps involved.

Back to `slice/2`:

```
iex> Enum.slice([0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10], 2..4)
[2, 3, 4]

iex> Enum.slice(0..20, 12..18)
[12, 13, 14, 15, 16, 17, 18]
```

Notice that the range is "inclusive", it includes all values from two to four, including four. Also keep in mind that indexes in Elixir are zero-based.

If no valid indexes can be found it will return an empty list.

```
iex> Enum.slice(0..20, 22..24)
[]
```

`slice/3` accepts an enum, an integer representing a starting index, and an integer representing a length.  It will then return a list of entries from the starting index to the end indicated by the length.

```
iex> Enum.slice(0..20, 15, 2)
[15, 16]

iex> num.slice(0..20, 22, 2)
[]
```

More here:
https://hexdocs.pm/elixir/Range.html
https://hexdocs.pm/elixir/Enum.html#slice/2
