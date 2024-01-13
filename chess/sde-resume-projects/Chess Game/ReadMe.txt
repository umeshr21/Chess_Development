ReadMe File

We will start by writing the header of the code with the required libraries – bits/stdc++.h.

The classes we will be creating for this project are as follows – GamePiece, PawnPiece, KnightPiece, BishopPiece, RookPiece, QueenPiece.

The GamePiece class will contain the common data and functions which will be shared by all the pieces in the game. We will create a  constructor for this class and it will take a char parameter PieceColor and will initialize the member variable mPieceColor. We will create a virtual function in this class called GetPiece() that returns a char representing the type of the piece. We will create boolean function IsLegalMove() which will take the source and destination positions of a move, and a pointer to a two-dimensional array GameBoard representing the current state of the game. The function checks if the move is legal and returns a boolean value indicating whether the move is legal or not.

The derived classes from the base class – GamePiece will override the GetPiece() function and then return the corresponding character for each piece type. The use the if-else control statements.

For the class PawnPiece, the if-else statement is used to choose between if the Destination square is unoccupied else the destination holds a piece of opposite color.

For the knightPiece class, the nested if statement is used to see if the destination square is unoccupied or occupied by opposite color.

For the BishopPiece class, we will make sure that all intervening squares are empty, we will check rows, columns and destination row.

Similarly for all the pieces we will define their functionality, how they will reach their destination by moving according to their specified rules.

In the class CBoard, we will allocate and place black pieces by using a for loop and also we will allocate and place white pieces. We will allocate different pieces to their positions on the chess board.

The Print() function will print out a representation of the chess board on the console. It will basically use two constants kiSquareWidth and kiSquareHeight to determine the width and height of each square on the board. It iterates across the board’s rows and columns, printing out the relevant characters to represent the border, numbering, and chess pieces.

The boolean type, IsInCheck() function takes a PieceColor parameter (either ‘w’ or ‘b’) and determines if the king of that color is now under control. It goes around the board, checking if any of the opponent’s pieces may lawfully move to the square housing the king. If this is the case, it returns true. If not, it returns false.

The boolean type, CanMove() function will examine a PieceColor parameter to see if any of the pieces of that color have a valid move on the current board. It will cycle around each square on the board and check for any legal moves that will not place the king of that color in check for each piece of that colour. It will return true if such a move exists. If not, it returns false.

We will create a class Chessboard which will display the board to play the chess game on. Creating a start() function to start the game using a do/while loop. Creating a GetNextMove() function, clear the screen and then display a welcome message along with keys to symbols used in the game to play. We will get the input and the convert to coordinates.

After that we will check that the indices are in range and that the source and destination are different. We will use if statements for additional checks for the piece color and valid destination and then make the move.

The boolean type, IsGameOver() function will check it the current player can move, we have a stalemate or checkmate. And the game will be over.

The main() function calls the start(0 function to start the chess game.
This sums up our project of Chess Game using C++.