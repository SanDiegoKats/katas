#February Monthly Meeting

There are a couple of options this time around. Pick 1. Pick 'em all. It's up to
you.

##Kata 1 - Hutton's Razor

This kata was taken from [Code Wars](http://www.codewars.com/kata/543833d86f032f0942000264),
and is also described in the following [paper](http://www.cs.nott.ac.uk/~pszgmh/semantics.pdf)

Hutton's Razor is a simple language that has exactly two pieces: integer constants
and an addition operation. In this kata you must develop an interpreter for it.

Here is an example AST for Hutton's Razor in Haskell

```
data Razor
  = Lit Int
  | Add Razor Razor
```

An an addition operation could be written, in Haskell, as

```
ex1 = Add (Lit 1) (Lit 2)

ex2 = Add (Lit 10) (Add (Lit 11) (Lit 12))
```

1. Implement an interpreter for Hutton's Razor. For example the program 
`Add (Lit 1) (Add (Lit 2) (Lit 3))` would return `6`.

2. Implement a pretty-printer; surround all `Add` operations with parenthesis. 
Spaces are not necessary. For example, the program `Add (Lit 1) (Lit 2)` would 
return `"(1+2)"`

##Kata 2 - Oragami

Folds are a family higher-order functions that process a data structure and build
up a return value. Many different data structures can be folded, but we'll focus
on lists for now.

The `foldr` function processes a list from right to left using an accumulator function
and and initial value. In Haskell, the type of `foldr` (when constrained to lists)
looks like this:

```
foldr :: (a -> b -> b) -> b -> [a] -> b
```

1. Implement `foldr`.

2. `foldr` is the basis for many of the most commonly know functions in FP. You can
use it to define `map`, `filter`, etc. Define the following list functions using `foldr`
   * `sum`, which calculates the sum of a list of integers
   * `length`, which returns the number of elements in a list
   * `minList` & `maxList`, which return the smallest and largest elements in a 
   list of integers.
   * `reverse`, which reverse a list
   * `map`, which takes a function that transforms an element of type `a` into 
   an element of type `b`, and a list of elements of type `a`, then returns a list
   of type `b`
   * `inits`, which returns all of the initial segments of a list. For example:
   `inits [1, 2, 3] = [[], [1], [1, 2], [1, 2, 3]]

##Kata 3 - Not Quite Lisp

This kata comes from from [Advent Of Code](http://adventofcode.com/day/1), though
we've changed the wording since it's no longer December.

UPS is trying to deliver packages in a large apartment building, but they can't 
find the right floor - the directions they received are a little confusing. The 
delivery person starts on the ground floor (floor 0) and then follows the 
instructions one character at a time.

An opening parenthesis, `(`, means he should go up one floor, and a closing 
parenthesis, `)`, means he should go down one floor.

The apartment building is very tall, and the basement is very deep; UPS will 
never find the top or bottom floors.

For example:

* `(())` and `()()` both result in floor `0`
* `(((` and `(()(()(` both result in floor `3`
* `))(((((` also results in floor `3`
* `())` and `))(` both result in floor `-1`, which is the first basement floors
* `)))` and `)())())` both result in floor -3

What floor do [these instructions](https://github.com/SanDiegoKats/katas/tree/master/2016-02-11/instructions.txt)
take UPS to.

What is the position of the first character that causes UPS to enter the basement?
The first character in the instructions is position 1, the second is position 2, 
and so on.

For example:

* `)` causes them to enter the basement at character position `1`.
* `()())` causes them to enter the basement at character position `5`

What is the position of the character that causes UPS to first enter the basement?
