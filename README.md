# Tennis Counting Dojo

![build status](https://github.com/ace-lectures/2aa4-tennis/actions/workflows/build.yaml/badge.svg)

- Author: Dr. [Sébastien Mosser](https://mosser.github.io)
- Version: 2024.01
- Context: McMaster University > Engineering > Computing & Software > SFWRENG > 2AA4
- License: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

## Problem Description

This problem is a classical Coding Dojo: [Tennis Coding Dojo](https://codingdojo.org/kata/Tennis/).
The objective is to implement a scoring system for a simplified version of tennis.

The scoring system is rather simple:

1. Each player can have either of these points in one game: `love`, `15`, `30`, `40`.
2. If you have `40` and you win the point you win the game, however there are special rules.
3. If both have `40` the players are _deuce_.
4. If the game is in _deuce_, the winner of a point will have _advantage_
5. If the player with _advantage_ wins the ball he wins the game
6. If the player without _advantage_ wins they are back at deuce.

### Assumptions

The problem description is vague and imprecise, and does not indicate how the score is actually 
incremented. We'll operate under the following assumptions:

- Players are characterized by a _strength_ (a simplification of their ATP ranking)/
- The _strength_ is an integer in the [0,100] range
- This number is provided to the counting assistant through the command line (default is 50)

## How to use this software?

To compile the source code into a turn-key _Java ARchive_ (JAR):

```
mosser@azrael 2aa4-tennis % mvn package  
```

To run the counting assistant:

```
mosser@azrael 2aa4-tennis % java -jar target/tennis.jar -p1 75 -p2 30
** Starting Tennis Counter Assistant
**** Reading Command-Line Arguments
****** P1's Strength is 75/100
****** P2's Strength is 30/100
**** Starting game
** TODO...
** Closing Tennis Counter Assistant
```
