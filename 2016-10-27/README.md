
# October Monthly Meeting

This month we have talk and a kata!

## Talk - PureScript & Pux

Speaker - Jesse Williamson

Functional programming is becoming very popular on the frontend. Libraries like React and Redux have done a lot to push functional ideals like purity & immutability into the mainstream. What about taking it even further? You may have heard of Elm and the number of benefits developers are getting using it. PureScript is another alternative to JavaScript. It is statically typed, and purely function like Elm, but is offers a few more features that make it a more powerful language. We'll take a look at the basics of the language, some of those extra features, and one of the libraries available for writing web frontends: Pux.

## Kata

### Kata 1 - Hutton's Razor++

This kata is a slightly modified version of Huttons Razor, taken from
[Code Wars](http://www.codewars.com/kata/543833d86f032f0942000264),
and is also described in the [this
paper](http://www.cs.nott.ac.uk/~pszgmh/semantics.pdf)

We're are going to describe a syntax tree for a simple language that has
exactly three pieces: literal integers, and addition operation, and a
multiplication operation.

Below is an example recursive data type (in Haskell) to model the AST:

```
data Expr =
    Lit Integer
  | Add Expr Expr
  | Mul Expr Expr
```

1. Implement an interpreter for this language. For example the program
`Mul (Lit 2) (Add (Lit 2) (Lit 3))` would return `10`.

2. Implement a pretty-printer; surround all `Add` operations with
parenthesis. Spaces are not necessary. For example, the program
`Mul (Lit 1) (Lit 2)` would return `"(1 * 2)"`

### Kata 2 - Oragami

Folds are a family higher-order functions that process a data structure and
build up a return value. Many different data structures can be folded, but we'll focus on lists for now.

The `foldr` function processes a list from right to left using an accumulator function and and initial value. In Haskell, the type of `foldr`
(when constrained to lists) looks like this:

```
foldr :: (a -> b -> b) -> b -> [a] -> b
```

The function `foldl` is very much like `foldr` but with a
[few differences](https:// wiki.haskell.org/Foldr_Foldl_Foldl'). Among
those differences is the order of arguments to the accumulator function,
and the fact that the list is process from left to right. The type of
`foldl` looks like this:

```
foldl :: (b -> a -> b) -> b -> [a] -> b
```

1. Implement `foldr`.

2. Implement `foldrl`

3. Folds are the basis for many of the most commonly know functions in FP.
You can use it to define `map`, `filter`, etc. Define the following list
functions using `foldr` or `foldl`

   * `sum`, which calculates the sum of a list of integers
   * `length`, which returns the number of elements in a list
   * `minList` & `maxList`, which return the smallest and largest elements
   in a list of integers.
   * `reverse`, which reverse a list
   * `map`, which takes a function that transforms an element of type `a`
   into an element of type `b`, and a list of elements of type `a`, then
   returns a list of type `b`
   * `inits`, which returns all of the initial segments of a list. For
   example:
   `inits [1, 2, 3] = [[], [1], [1, 2], [1, 2, 3]]`
