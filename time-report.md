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
    
   
