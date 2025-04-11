# Time Report

> Write about what you have done and how long you have worked on each part of the project.

For example: 

- 2025-03-26 14:00 Worked for 3 hours.
  - 3 arrays:
    - 1 to store the opening board
    - 1 to store the name of the squares
    - 1 to store the name of the pieces, for future use
  - 2 buttons:
    - 1 to start the next turn
    - 1 to update the board
  - 2 functions
    - 1 that prints the the board
    - 1 that controls the player turns. Including prompts and if-statements.
   
- 2025-03-27 12:40 Worked for 3 hours.
  - Polished the layout of the game board
    - Added monospace style
    - Made the squares with []
  - 2 arrays
    - 1 for unmoved pawns; so I could make them be able to go 2 squares
    - 1 for legal moves; so the program can restrict how the pieces can move
  - 8 new functions 
    - 2 for the different players turns (because I'm using text the program checks for lowercase characters for white and uppercase for black)
    - 6 for the different pieces to control how they can move
  - Movement restrictions in the Pawn function
    - Implemented how they can move forward
  - 1 while-loop
    - Checks if the player wants to make a legal move and implement that to the game board
  - 1 for-loop
    - Changed how the board is being printed, with a for-loop
   
  - 2025-03-29 15.00 Worked for 2 hours.
    - Changed name on the chessPieces array to startBoard for better workflow
    - Changed the PawnMovement function
      - Added diagonaly movement when an enemy piece is diagonaly in front of the pawn
    - Fixed a bug with removing of elements in the unmovedPawns array
    - 1 function
      - UpgradePiece()
      - Added so the pawns upgrades to a queen when reaching the other side of the board
     
  - 2025-04-02 12.30 worked for 4 hours
    - Changed the UpgradePiece function so the player gets to chose what piece they want to upgrade the pawn to
    - Implemented movement restrictions for the black rooks
      - Contains 4 if-statements, 1 for each direction
      - It checks if there is a free square or an enemy pawn next to the piece and adds that square to the legalMoves array
      - Then by using a while loop it does that for every square until it hits a "stop"
     
  - 2025-04-03 14.30 Worked for 2.5 hours
    - Cleaned up the code in Rook Function
      - 2 new variables so I could shorten the code
        - enemyPiece
        - friendlyPiece
        - Depending on what players turn it is the two variable is assigned to the whitePieces and blackPieces arrays 
    - Bugfixes
      - The rook-movement was wrong, they could move to places where they were not supposed to be able to move to
     
  - 2025-04-04 15.00 Worked for 2 hours
    - 4 functions
      - KnightMovement
        - Contains 8 if-statements
      - BishopMovement
        - Contains 4 if-statements with a while-loop in each
      - KingMovement
        - Contains 8 if-statements. 1 for each direction
      - QueenMovement
        - Contains 2 function-referenses, 1 to RookMovement and 1 to BishopMovement
    - Removed unnecessary code from the RookMovement function
   
  - 2025-04-10 8.00 Worked for 2.5 hours
    - Checked if the movement of the pieces works
      - Fixed bugs:
        - Bishops and Rooks; the while-loops added squares to the legalMoves-array above or under the squareNames index range
    - 1 function
      - Created the PieceChooser function
      - This was made so that the player is not asked again what piece they want to move when the program is checking for what squares the king would be in check
  - 2025-04-10 16.00
    - 1 function
      - Merged the WhiteTurn- and the BlackTurn-functions to the MovementManager-function
      - This was made to get lesser code. Instead of having two function doing pretty much the same thing, now only one function mange it instead
     
  - 2025-04-11 9.00 Worked for 2 hours
    - 2 variable
      - pieceVar
      - kingSlayer
        - to be able to check for check the program needs to run through all the enemies possible moves to determine which ones that would make the king check.
        - therefore I had to make a varible that could change depending on if the program needs to check for the possible moves a piece can make (chosenPiece)
        - or if the program needs to determine wich enemy pieces that could make the king check (kingSlayer)
    
   
