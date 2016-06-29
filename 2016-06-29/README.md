May Monthly Meeting
===================

This month we have talk and a kata!

Talk - A Beginners Introduction To Idris
---------------------------------

Speaker - Jesse Williamson

"Idris is a general purpose pure functional programming language with dependent types." This means that types can be predicated on values. For example, you can define the concatenation of two lists in such a way that the compiler enforces the length of the resulting list to be the sum of input lists. But there is even more that can be done with dependent types.

This talk will start at the basics and stay there for the most part. This isn't a deep dive but is intended to pique your interest in this cool language.

Kata - Robot Simulator
----------------------

_Taken from [exercism.io](http://exercism.io/exercises/haskell/robot-simulator/readme)._

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
