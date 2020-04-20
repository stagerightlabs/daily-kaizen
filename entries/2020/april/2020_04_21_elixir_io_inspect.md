Topic of the Day: Elixir's `inspect/2` method from the `IO` module.

Elixir's `IO` module provides a set of tools for reading and writing from the console (stdin/stdout.)

When working with Elixir you may often need to inspect an object at various points during code execution.  You may be tempted to use the `IO.puts/2` method to print the object to stdout; however this will fail for structs that haven't defined how they should be represented as strings.

To facilitate debugging we can make use of `IO.inspect/2` which will take any value and print it to the console. It will treat custom structs as maps and print their contents in a similar fashion.

For example:

```
iex> m = %{foo: "bar"}
iex> IO.inspect(m)
%{foo: "bar"}
```

The second parameter for `IO.inspect/2` is optional; it will let you specify a "label" to help find specific content in the stdout output:

```
iex> m = %{foo: "bar"}
iex> IO.inspect(m, label: "baz")
baz: %{foo: "bar"}
```

Elixir has an amazing feature that will let us "chain" functions together with the pipe operator "|>".  The pipe operator will take the output of the previous function and pass it in as the first parameter of the next function, like so:

```
iex> %{foo: "bar"}|>Map.put(:baz, "bat")
%{baz: "bat", foo: "bar"}
```

`IO.inspect/2` can be used in a chain of functions to help with debugging.  Conveniently, it will return whatever value it receives, so it won't break the chain:

```
iex> %{foo: "bar"}
...> |>IO.inspect(label: "before")
...> |>Map.put(:baz, "bat")
...> |>IO.inspect(label: "after")
before: %{foo: "bar"}
after: %{baz: "bat", foo: "bar"}
```

Function chaining is a very powerful concept; a cornerstone of functional programming.  Once you have wrapped your head around the idea it will change how you think about structuring code.
