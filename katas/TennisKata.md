# Tennis kata

https://en.wikipedia.org/wiki/Tennis_scoring_system

Create a program that can keep track of score in a tennis match based on the rules above.

This is a [TDD](https://en.wikipedia.org/wiki/Test-driven_development) kata so write one or more test before code for each business rule.

## The program's interface

1. The program needs to be created with the names of the two players.
2. When a player scores a point a method called point should be called with the players name.
3. At all times a method called scores can be called to retrieve the current score.

## Business rules

1. The program needs to be created with exactly two players and names should be defined.
2. The proram should throw an exception if a point is given to a player that does not exists.
3. The score should be `love-love` if no one have scored a point.
4. The score should be `15-love` if player 1 scored a point and opposite it player 2 scored first.
5. The score should be `X-all` if the score is 15-15 or 30-30 where X is either 15 or 30.
6. The score should be `deuce` if the score is equal and both players have 3 points or more.
7. The program should support scores like `40-love`, `40-15`, `40-30`, `30-15`, `15-30` and other normal scores.
8. If one players have minimum 4 points and the other is one point behind the score should be `advantage player1` where player1 should be the name of the player.
9. The game should end then one player have atleast 4 points and have 2 points more than the other.
10. Trying to award a player with a point after game ends should throw an exception with message `"The game have ended, no point can be given"`
11. If the score method is called after the game have ended then it should display the winner.
