# ThreeInALineAssembly
Assembly Code to create a playable connect three game

 

Dillon Carter 

Michael Higley 

Outline: 

Store output of board as a string 

2d array stores state of board, each board place represented by 2 bits, 00 nothing, 01 Red, 10 Blue, user is always Red and computer is always blue 

3 x 6 Board, AI will randomly choose a spot on the board 

Inputs from the user will be 1, 2, or 3 depending on the column they want 

Piece must fall to place above where last piece rests 

Ensure that user input is valid, otherwise, output what they inputted incorrectly 

Possible errors: Invalid range for columns, column is full 

 

Each Game Tick: 

Get current Player,  

IF player is user, prompt user for input, if error, print error message 

If player is computer, get random num (1-3) to put new piece and ensure it is legal move 

Iterate through array and convert the state of the position on the board to the player 

Iterate once again and check if the state of any three pieces matches a game win state 

If so, find who won, output, and exit 

Otherwise, branch back to top of game tick and continue 

 

Methods: 

IncrementGameTick() 

UserInput(prompts user for input) 

CheckValid(check if the move is valid) 

ChangeState(Change state of board position to player) 

IfMatch(Check if there is a winning move) 

OutputCompWin() 

OutputPlayerWin() 

OutputYouSuck() 

 

Variables: 

Strings: User Wins, Computer Wins, Game tie (You suck), Blue piece, Red Piece, Complete board, Input position, Error, Invalid column, column full, 

Ints: Current Game tick, last user column, size of columns, size of rows,  

Array: 6 Array of 3 columns,  

 

Description of the Project: The program is a MIPS assembly program based on the game Three in a Line. The goal of the game for each player is to get 3 pieces in a row on the board, whether it be horizontal, vertical, or diagonal. Players take alternating turns to enter which column to drop their piece in. The game ends when one player gets three pieces in a row or the board fills up completely without a win. In that case, the game ends in a tie. 
