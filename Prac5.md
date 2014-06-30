
Game 2048 - Test Plan
=====================
Introduction
------------
The game 2048 is played by a user with the intent to rotate the board in one of the four directions – left, right, up and down.
When the user tilts the board, the numbers move from one position to another. However, if two cells contain the same value, 
the cells are merged. This new cell contains a value equal to the value obtained by adding the values of the original cells. 
At the beginning of the game, the board contains two cells, containing value 2 and they are placed at random positions on 
the board. Besides this, whenever the board is rotated, a new cell, with a value 2 or 4, is added at a random place. In case
a merger occurs, the score of the player is incremented by a value equal to the value of merged cell. The objective of 
the game is to get a cell with a value equal to 2048. If the board becomes full and there is no place for any new cells,
then the game is considered to be over.  

Software Specifications
------------------------
•	Java development toolkit version 7
•	NetBeans IDE version 7.3
•	Github account
•	Internet connection


Test Scenarios
--------------
I.	Game Board Rendering
-------------------------
The first test scenario investigates if the initial game grid is rendered properly or not. The points to be checked include:
1.	The grid must appear as a matrix of four columns and rows. 
2.	The grid must contain only two filled cells at this time. 
3.	The location of the filled cells must be randomly selected.
4.	The value of the filled cells must be equal to two.

II.	Verification of User Input
-------------------------------
This test scenario checks if the program is capable of verifying the user input given. The points to be checked include:
1.	If the user enters l, r, t, d, or x, the input is valid.
2.	If the user enters any other input other than the ones mentioned above, the input must be considered as invalid.
3.	If the input entered is invalid, the user must be notified about the error using an error message. 

III.	Handling User Input
-------------------------
This test scenario checks if the program is capable of handling the valid user input correctly. The points to be checked include:

Tilting in Right Direction
As part of this scenario, the tilting functionality of the program is checked. Whenever the user enters ‘r’, 
the following should occur:
1.	There must not be any movement of cells if:
i.	The board is full.
ii.	All the cells of the board are already right aligned
2.	If there is a free cell, the cells to the left of this cell should move to their right.
3.	If the rightmost cells are free, all the cells must move to their right.

Tilting in Left Direction
As part of this scenario, the tilting functionality of the program is checked. Whenever the user enters ‘l’, the following should occur:
1.	There must not be any movement of cells if:
a)	The board is full.
b)	All the cells of the board are already left aligned
2.	If there is a free cell, the cells to the right of this cell should move to their left.
3.	If the leftmost cells are free, all the cells must move to their left.

Tilting in Top Direction
As part of this scenario, the tilting functionality of the program is checked. Whenever the user enters ‘t’, the following should occur:
1.	There must not be any movement of cells if:
	The board is full.
	All the cells of the board are already right aligned
2.	If there is a free cell, the cells below this cell should move upwards.
3.	If the topmost cells are free, all the cells must move upwards.

Tilting in Down Direction
As part of this scenario, the tilting functionality of the program is checked. Whenever the user enters ‘d’, the following should occur:
1.	There must not be any movement of cells if:
•	The board is full.
•	All the cells of the board are already right aligned
2.	If there is a free cell, the cells above this cell should move downwards.
3.	If the bottommost cells are free, all the cells must move downwards.

IV.	Managing Cell Merger
------------------------
In case, two adjoining cells contain the same value, they must be merged into one cell. This scenario checks the following:
1.	Cells must be merged if adjacent cells contain the same value.
2.	The value of the new cell is equal to the value obtained by adding the values of the two original cells. 

V.	Maintaining Score
---------------------
This scenario checks if the program is able to maintain the player score properly. As part of this test scenario,
the following must be tested:
1.	The score is initialized to zero at the beginning of the game.
2.	Upon cell merger, score is incremented by a value equal to the value of the cell formed after merger. 

VI.	Game Termination
--------------------
Game termination can occur in two scenarios. Firstly, the user may choose to exit the game by entering ‘x’. 
On the other hand, the game may also be declared over if the game is won or lost by the player. As part of this scenario,
the second facet of game termination is tested as the first facet is tested in one of the previous test scenarios,
which involves testing input handing. In this case, the game should be declared over in one of the following cases:
1.	No cell is free or the player loses the game.
2.	One of the cells has attained the value of 2048 or the player wins the game. 

If there is no more free cell so it is game over, application should notify user with game over message, and game is stopped.

Dependencies, Risks and Limitations
--------------------------------------
There are several dependencies and risks associated with the project. One of the fundamental dependencies involves
the understanding of the game and its rules. A poor understanding of the game rules and conventions shall act as a barrier 
in smooth functioning of this phase of the project. 
It is likewise important to state that the following is beyond the scope of this program.
•	Multi-player game
•	Multi-level game
•	User cannot change the settings of the game
•	Networking and online game play 
