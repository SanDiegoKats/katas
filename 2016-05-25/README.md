May Monthly Meeting
===================

Here are a couple of different options this month. Some are a little longer than
others. Feel free to do whichever one(s) you like.

Kata 1 - Reverse Polish Notation Calculator
-------------------------------------------

Create a calculator which evaluates expressions written in [Reverse Polish Notation](https://en.wikipedia.org/wiki/Reverse_Polish_notation)

For example `5 1 +` is equal to `5 + 1` and should evaluate to `2`. A more complex example `5 1 2 + 4 * +  3 -` is equal to `5 + ((1 + 2) * 4) - 3`.

There will always be spaces between numbers an operators; you don't need to account of `51+` it will represented as `5 1 +`.

The only valid operators are `+`, `-`, `*` and '/'.

You won't be thrown any curveballs, such as dividing by zero.

_Borrowed from [Code Wars](http://www.codewars.com/kata/reverse-polish-notation-calculator)_

Kata 2 - Towers of Hanoi
------------------------
From [Wikipedia](https://en.wikipedia.org/wiki/Tower_of_Hanoi)

> The Tower of Hanoi (also called the Tower of Brahma or Lucas' Tower,[1] and sometimes pluralized) is a mathematical game or puzzle. It consists of three rods, and a number of disks of different sizes which can slide onto any rod. The puzzle starts with the disks in a neat stack in ascending order of size on one rod, the smallest at the top, thus making a conical shape.

> The objective of the puzzle is to move the entire stack to another rod, obeying the following simple rules:

> 1. Only one disk can be moved at a time.
> 2. Each move consists of taking the upper disk from one of the stacks and placing it on top of another stack i.e. a disk can only be moved if it is the uppermost disk on a stack.
> 3. No disk may be placed on top of a smaller disk.

Write a function that takes a number of disks and names for three pegs (as strings) and returns a list of moves to be performed to move the stack from the first peg to the second.


For example:
```
hanoi(2, 'a', 'b', 'c'); // => [['a', 'c'], ['a', 'b'], ['c', 'b']]
```

Kata 3 - I Was Told There Would Be No Math
-------------------------
_Adapted from [Advent of Code](http://adventofcode.com/day/2)_

You're charge of wrapping gifts at the local department store and are running
low on wrapping paper, and so you need to submit an order for more. You've got
a large order coming through and you don't want to order more paper than you need.
Luckily, you have a list of the dimensions (length l, width w, and height h) of
each present so you can figure out exactly how much to order

Every present is a box (a perfect right rectangular prism), which
makes calculating the required wrapping paper for each gift a little easier:
find the surface area of the box, which is `(2 * l * w) + (2 * w * h) + (2 * h * l)`, but you also
need a little extra paper for each present: the area of the smallest side.

For example:

A present with dimensions 2x3x4 requires `(2 * 6) + (2 * 12) + (2 * 8)` = 52 square feet of
wrapping paper plus 6 square feet of slack, for a total of 58 square feet.

A present with dimensions 1x1x10 requires `(2 * 1) + (2 * 10) + (2 * 10)` = 42 square feet of
wrapping paper plus 1 square foot of slack, for a total of 43 square feet.

All numbers in the your list are in feet. How many total square feet of wrapping
paper should they order?

Kata 4 - Log Parsing
--------------------

_Taken from [CIS194 Spring 2013]( http://www.seas.upenn.edu/~cis194/spring13/
  lectures.html) Week 1 homework_
> We’re really not sure what happened, but we did manage to recover
the log file error.log. It seems to consist of a different log message
on each line. Each line begins with a character indicating the type of
log message it represents:

> * `I` for informational messages,
> * `W` for warnings, and
> * `E` for errors.

> The error message lines then have an integer indicating the severity
of the error, with 1 being the sort of error you might get around to
caring about sometime next summer, and 100 being epic, catastrophic
failure. All the types of log messages then have an integer time stamp
followed by textual content that runs to the end of the line. Here is a snippet
of the log file including an informational message followed by a level 2 error
message:

> ```
I 147 mice in the air, I’m afraid, but you might catch a bat, and
E 2 148 #56k istereadeat lo d200ff] BOOTMEM
```

> It’s all quite confusing; clearly we need a program to sort through
this mess.

You need to parse each line of [the file](data/error.log) an create an appropriate `LogMessage`
from it. Each `LogMessage` with have a "type" (error, info or warning with
errors having a corresponding error code), a timestamp and a message. It is also
possible that the file contains a entry that is unknown. In this case, the
parsing function needs to return some type of `Unknown` message and the text of
the message.

1. Define a function that can read a line from the error file, and parse it into
a `LogMessage`

2. Define a function that can parse an entire file and return a list of
`LogMessage`

Kata 5 - Conway's Game of Life
------------------------------

In this kata you will calculate a single generation in
[Conway's Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life).
You will be given the dimensions of a finite two dimensional grid, in which each
cell is either alive or dead, and list of currently live cells. Using the
following rules, calculate the next state of the grid.

1. Any live cell with fewer than two live neighbors dies, as if caused by underpopulation.
2. Any live cell with more than three live neighbors dies, as if by overcrowding.
3. Any live cell with two or three live neighbors lives on to the next generation.
4. Any dead cell with exactly three live neighbors becomes a live cell.

For example the input a 4x8 grid with live cells at `[2, 5], [3, 4], [3, 5]`
would be visualized as:

```
........
....*...
...**...
........
```

Calculating the next generation in the game based on the state above would look like
`life(4, 8, [[2,5], [3,4], [3,5]])`. The function should return a list of live cells:
`[[2, 4], [2,5], [3,4], [3,5]]` which could be visualized as:

```
........
...**...
...**...
........
```

_Example taken from [Coding Dojo](http://codingdojo.org/cgi-bin/index.pl?KataGameOfLife)_
