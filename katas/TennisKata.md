# Tennis kata

https://en.wikipedia.org/wiki/Tennis_scoring_system

Create a program that can keep track of score in a tennis match based on the rules above.

This is a [TDD](https://en.wikipedia.org/wiki/Test-driven_development) kata so write one or more test before code for each business rule.

## The program's interface

1. The program needs to be created with the names of the two players.
2. When a player scores a point a method called `point(name)` should be called with the players name.
3. At all times a method called `scores()` can be called to retrieve the current score.

## Business rules

1. The program needs to be created with exactly two players names as strings.
1. The program should throw error if not created with exactly two names.
1. The `score()` method should return `love-love` if no one have scored a point.
1. The `score()` method should return `15-love` if player 1 have one point and player 2 have zero points.
1. The `score()` method should return `love-15` if player 2 have one point and player 1 have zero points.
1. The program should throw an error if a point is given to a player that does not exists.
1. The `score()` method should return `X-all` if the score is 15-15 or 30-30 where X is either 15 or 30.
1. The `score()` method should return `deuce` if the score is equal and both players have 3 points or more.
1. The program should support scores like `40-love`, `40-15`, `40-30`, `30-15`, `15-30` and other normal scores.
1. If one player have minimum 4 points and the other is one point behind the `score()` should be `advantage player1` where player1 should be the name of the player.
1. The `score()` should return `game over - player X won` when one player have at least 4 points and have 2 points more than the other. X being the winning players name.
1. Trying to award a player with a point after game ends should throw an error with message `"game over - no points can be given"`
