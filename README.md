# APS-105-Lab-6-Battleship
APS 105 Lab #6: Battleship

**Download Link:https://programming.engineering/product/aps-105-lab-6-battleship/**

Description
5/5 – (2 votes)
Important note: You must use the submit command to electronically submit your solu-tion by the end of your lab session.

In this lab, you will write parts of a C program / application that plays a game of Battle-ship. By the end of this lab, you should be able to:

Use two dimensional arrays. Use functions for efficiency.

Problem Statement

Your part of the program will be to create a function that sets up the boards for the game. In use one board will be set up according to user (“Player”) input, another will be randomly generated for the opponent.

For our game, the board will be 9 squares down (rows denoted 1-9) and 11 squares wide (columns denoted 1-11). The game is played with two players, one of which will be the computer in our version. Each player places “ships” on non-overlapping areas, either verti-cally or horizontally on their board. Each player in turn calls out a square. If it is occupied by one of the other player’s ships then it is a “hit” otherwise it is a “miss”. Play continues until one player hits every square occupied by ships of their opponent.

We will play the game with one each of the following ships (one set per player):

Ship Name

Ship Size

Carrier

5

Battleship

4

Destroyer

3

Submarine

2

Patrol Boat

1

You can find out more about the game and example boards at

https://en.wikipedia.org/wiki/Battleship(game)

The following are the requirements of the function you will write:

Function will be able to populate a board either based on user input or using random placement. Which is done is selected by a parameter.

When used: Inputs from the player for each ship size will be: Row, Column, Orienta-tion. The Ship Size will be 1-5, Row will be 1-9, Column will be 1-11, Orientation will be 0 for horizontal (going to the right from the Row/Column position) or 1 (going down from the Row/Column position).

Function must check that inputs are valid, but all inputs will be integer

Function must not allow ship overlap or ships to extend past the edges of the board.

Function to conform to the following declaration as given in the skeleton code pro-vided:

void populateBoard(bool getUserInput,

int board[BOARDROWS+1][BOARDCOLS+1]);

where

If getUserInput is true, populate the board using input from a player.

If getUserInput is false, populate the board randomly.

and board is the board to be populated. BOARDROWS is 9; BOARDCOLS is 11 (These are fixed values)

Cells in the board will be assigned the following values: 0 if empty, otherwise the size of the ship covering the cell (so 3 if a Destroyer is covering that cell, since a Destroyer takes three cells in all and this is one of the three)

Examples

Please see the accompanying file of examples. The computer’s playing is guided using the random numbers. See the note below on generating the computer board.

Notes

You can run your completed routines in the program shell provided to continue from the board generation into game play! Or you might want to program the whole thing

– it’s under 200 lines of code!! (But be sure to use the given game code for your submission.)

Suggestion: Make a chart of all the possible responses to any player input, including all the “problem” conditions, trace your code to make sure you’ve covered all these conditions, then test your code for each case.

You may want to play with the code given to make the development easier in the following ways. Make sure that you change the program back before you submit it!

Put a loop in to run your program repeatedly.

Cut out or comment out the part of the program to play the game so you only get the part that populates the board. This populating part is in main() until the comment

play starts here

Note that you also can stop program execution at an input with a control-C.

You can temporarily set dumpComputer=true; (a boolean variable initialized to false) to cause the computer’s board to be printed at the start of the game. You may be asked to do this by the TA. Be sure to remove this for testing and submission.

On Examify a user board then computer board are printed and the game is not played.

To correctly generate the computer board: Use the same order of ship placement as for the user (ie ship 5 first, then 4, 3 etc.) and generate the parameters in the same order as for user input (row, column, orientation) using a single use of getRand() for each parameter and you will pass the computer board in the test cases.

Grading / Submission and Automarking

In a file called Lab6.c, write your solution to the problem. There are ten (10) marks available in this lab.

Read the notes and other comments carefully to make sure your automarked version con-forms to expectations.

The total of 10 marks on this lab are marked in two different ways:

By your TA, for 4 marks out of 10. Once you are ready, show your program to your TA so that we can mark your program for style, and to ask you a few questions to test your understanding of what is happening.

The TA will also ask you some questions to be sure that you understand the under-lying concepts being exercised in this lab.

By an auto-marking program for 6 marks out of 10. You must submit your function through Examify for marking.

Important Note: You must submit your lab by the designated time and date. Late sub-missions will not be accepted, and you will receive a grade of zero.

Code submitted into Examify will automatically be saved. You can run the test function against some test inputs on that platform, as you did for Lab 5.

3
