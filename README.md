#Hog Game Progect
In this project, I developed a simulator and multiple strategies for the dice game Hog. 
I used control statements and higher-order functions together. 
##Topics covered:
1. Elements of Programming
2. Defining New Functions
3. Designing Functions
4. Control
5. Higher-Order Functions

##The idea:
In Hog, two players alternate turns trying to be the first to end a turn with
at least 100 total points. On each turn, the current player chooses some number 
of dice to roll, up to 10. That player's score for the turn is the sum of the dice outcomes.

##Game strategies:  
To spice up the game, we will play with some special rules:

* **Pig_Out** If any of the dice outcomes is a 1, the current player's score for the turn is 0.
* **Piggy Back** When the current player scores 0, the opposing player receives points equal to the 
number of dice rolled that turn.
    * Example: If the current player rolls 3 dice that come up 1, 5, and 1, then the current player 
      scores 0 and the opponent scores 3.
* **Free Bacon** A player who chooses to roll zero dice scores one more than the largest digit in the opponent's total score.
    * Example 1: If the opponent has 42 points, the current player gains 1 + max(4, 2) = 5 points by rolling zero dice.
    * Example 2: If the opponent has has 48 points, the current player gains 1 + max(4, 8) = 9 points by rolling zero dice.
    * Example 3: If the opponent has has 7 points, the current player gains 1 + max(0, 7) = 8 points by rolling zero dice.
* **Hog Wild** If the sum of both players' total scores is a multiple of seven (e.g., 14, 21, 35), then the current player rolls four-sided dice instead of the usual six-sided dice.
* **Hogtimus Prime** If a player's score for the turn is a prime number, then the turn score is increased
to the next largest prime number. For example, if the dice outcomes sum to 19, the current player scores 
23 points for the turn. This boost only applies to the current player. Note: 1 is not a prime number!
* **Swine Swap** After the turn score is added, if the last two digits of each player's score are the reverse of each other, the players swap total scores.
    * Example 1: The current player has a total score of 13 and the opponent has 91. The current player rolls two dice that total 6. The last two digits of the current player's new total score (19) are the reverse of the opponent's score (91). These scores are swapped! The current player now has 91 points and the opponent has 19. The turn ends.
    * Example 2: The current player has 66 and the opponent has 8. The current player rolls four dice that total 14, leaving the current player with 80. The reverse of 80 is 08, the opponent's score. After the swap, the current player has 8 and the opponent 80. The turn ends.
    *Example 3: Both players have 90. The current player rolls 7 dice that total 17, a prime that is boosted to 19 points for the turn. The current player has 109 and the opponent has 90. The last two digits 09 and 90 are the reverse of each other, so the scores are swapped. The opponent ends the turn with 109 and wins the game.

