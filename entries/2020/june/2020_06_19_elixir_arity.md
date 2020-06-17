Topic of the Day: "Arity" in Elixir

The "arity" of a function refers to how many parameters it accepts. In the elixir ecosystem it is most often deliminated by a slash after the function's name.  For instance, there are two `sort` methods in the Enum module: `Enum.sort/1` and `Enum.sort/2`.  The first takes only one parameter and the second takes two. In other languages this is sometimes referred to as function "overloading".

Arity is important to think about.  Even though those two sort methods are on the same module and have the same name, Elixir sees them as being completely different and unrelated.  So different in fact, that it can't infer your true intention if you accidentally omit a parameter. I often find error messages that say "`Enum.sort/0` does not exist" because I happened to forget to pass in the right parameter. The compiler was not able to infer my intentions. Granted, that is not its job, but my point is that you have to be very thoughtful about your parameter usage or you might find yourself facing unexpected errors.

More here:
https://blog.tentamen.eu/function-arity-in-elixir/
