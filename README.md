# go-life

This is go-life. It is a board game and a mixture between go and Conway's game of life.

[You can play it here](https://mancomb.github.io/go-life/index.html)

## About the rules
- Similar to go, two players alternately put pieces (black and white) on empty fields on the board.
- However, there is an additional game phase after each player has made a move. The "life-phase". 
- The goal is to have more space conquered at the end of the game than the opponent, but different to go, simply the total number of black vs white pieces that are placed on the board is relevant to decide who has won. 
- There are no capture moves. Instead pieces may be 'killed' in the life-phase of each round.
- It is not possible to pass a move.
- The game ends when all the board is covered with pieces.
- The game also ends when a board position repeats itself 3 times in succession.
- When the game ends, the player with more pieces of his color on the board wins. A draw is also possible.
- There are two game parameters, "kill threshold" and "growth threshold", which determine the life-phase.
- In the life-phase, a similar ruleset as in Conway's game of life is applied:
  - For each field, each of the 8 neighboring fields is considered.
  - The difference between the number of black and white neighboring pieces is calculated.
  - If the field is empty and the difference is larger or equal to the growth threshold, the field gets a black piece.
  - If the field is empty and the difference is smaller or equal to the negative growth threshold, the field gets a white piece.
  - If the field is white and the difference is larger or equal to the kill threshold, the white piece is removed (killed).
  - If the field is black and the difference is smaller or equal to the negative kill threshold, the black piece is removed (killed).
  - Else, the field remains unchanged.
  
  
*Gunnar Klämke, April 2020*
