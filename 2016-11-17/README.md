# November Monthly Meeting

This month we're going to try something new. We're featuring katas from [exercisim.io](http://exercism.io/). There are 5 to choose from:

## Difficulty: Easy

### [Bob](http://exercism.io/exercises/haskell/bob/readme)

> Bob is a lackadaisical teenager. In conversation, his responses are very limited.
>
> Bob answers 'Sure.' if you ask him a question.
>
> He answers 'Whoa, chill out!' if you yell at him.
>
> He says 'Fine. Be that way!' if you address him without actually saying anything.
>
> He answers 'Whatever.' to anything else.

Write a program that will give the correct response for an input phrase.

If the phrase is a normal question, Bob responds 'Sure'.

If the phrase is in all capital letters, Bob responds 'Whoa, chill out!'.

If the phrase is empty, Bob responds 'Fine. Be that way!'.

For everything else, Bob responds 'Whatever.'.

### [Leap](http://exercism.io/exercises/haskell/leap/readme)

Write a program that can take a year and tell you if it is a leap year.

A leap year, in the Gregorian calendar, occurs

> On every year that is evenly divisible by 4
>
> Except every year that is evenly divisible by 100
>
> Unless the year is also evenly divisible by 400

## Difficulty: Medium

### [Hamming](http://exercism.io/exercises/haskell/hamming/readme)

> Write a program that can calculate the Hamming difference between two DNA
> strands.
>
> A mutation is simply a mistake that occurs during the creation or copying
> of a nucleic acid, in particular DNA. Because nucleic acids are vital to
> cellular functions, mutations tend to cause a ripple effect throughout
> the cell. Although mutations are technically mistakes, a very rare
> mutation may equip the cell with a beneficial attribute. In fact, the
> macro effects of evolution are attributable by the accumulated result of
> beneficial microscopic mutations over many generations.
>
> The simplest and most common type of nucleic acid mutation is a point
> mutation, which replaces one base with another at a single nucleotide.
>
> By counting the number of differences between two homologous DNA strands
> taken from different genomes with a common ancestor, we get a measure of > the minimum number of point mutations that could have occurred on the
> evolutionary path between the two strands.
>
> This is called the 'Hamming distance'.
>
> It is found by comparing two DNA strands and counting how many of the
> nucleotides are different from their equivalent in the other string.

```
GAGCCTACTAACGGGAT
CATCGTAATGACGGCCT
^ ^ ^  ^ ^    ^^
```

Note: The Hamming distance is only defined on sequences of equal length.

### [Robot Simulator](http://exercism.io/exercises/haskell/robot-simulator/readme)

Write a robot simulator.

A robot factory's test facility needs a program to verify robot movements.

The robots have three possible movements:

  * turn right
  * turn left
  * advance

Robots are placed on a hypothetical infinite grid, facing a particular direction
(north, east, south, or west) at a set of {x,y} coordinates, e.g., {3,8}, with
coordinates increasing to the north and east.

The robot then receives a number of instructions, at which point the testing
facility verifies the robot's new position, and in which direction it is
pointing.

The letter-string "RAALAL" means:

  * Turn right
  * Advance twice
  * Turn left
  * Advance once

Say a robot starts at {7, 3} facing north. Then running this stream of
instructions should leave it at {9, 4} facing west.

## Difficulty: Hard

### Minesweeper

Write a program that adds the numbers to a minesweeper board

> Minesweeper is a popular game where the user has to find the mines using
> numeric hints that indicate how many mines are directly adjacent
> (horizontally, vertically, diagonally) to a square.
>
> In this exercise you have to create some code that counts the number of
> mines adjacent to a square and transforms boards like this (where `*`
> indicates a mine):

```
+-----+
| * * |
|  *  |
|  *  |
|     |
+-----+
```
> into this

```
+-----+
|1*3*1|
|13*31|
| 2*2 |
| 111 |
+-----+
```
