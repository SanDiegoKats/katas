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
