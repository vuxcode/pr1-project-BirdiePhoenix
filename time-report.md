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
       
  - 2025-04-11 13.30 Worked for 2 hours
    - Tried to insert a textbox and rearrange the buttons
      - It didn't go well so I had to restart from the last save and take it step by step
    - Added 1 Start button and 1 function
      - It activates a StartGame-function wich hides the startbutton and shows the TakeTurn-button
    - Removed the updateBoard-button since the board now updates automaticly
    - Added 1 more infotext in preparations to replace the prompts with textboxes
    - Changed so the player turns now shows in HTML in the info text at the top instead of showing up as prompts  
    
   - 2025-04-12 11.30 Worked for 0.5 hour
     - Added a textbox
     - Made it possible to change the second infotext
     - Changed the prompt that asked for what piece to innerHTML
    
   - 2025-04-13 22.00 Worked for 1.5 hours
     - Added 1 button and changed 1 button
       - Added a button to confirm the choice of square
       - Changed the turnButton to pieceButton wich confirms the choice of piece
     - 3 functions
       - StartGame:
         - Hides the startButton and the squareButton and shows the pieceButton and the textbox and then goes to TurnOrder
       - BetweenPieceAndSquare:
         - Hides the pieceButton and shows the squareButton. infoText2 is changed to ask what square the piece should be moved to.
       - SquareChooser:
         - Defines the chosenSquare variable and makes it upperCase.
         - Moved the legalMoves loop here from EndTurn.
         - Removed the while-loop and kept the if-statement. If legalMoves include the chosen square the EndFunction is also being runned
         - but if not we'll go back to the BetweenPiecAndSquare function.
     - Changed the TurnOrder function
       - It now only defines the enemyPieces and friendlyPieces variables and changes the top text to wich players turn it is and the bottom text
       - to ask what piece the player wants to move. To continue to the PieceChooser function the player needs to press the confirmPiece button
     - Changed the PieceChooser function
       - It now defines the chosenPiece variable
       - changes the chosenPiece variable to upper- or lowercase
       - runs the MovementManager and then the BetweenPieceAndSquare functions
     - Changed the EndTurn function:
       - Removed everything except from UpgradePiece(); to PrintBoard();
       - Added so the StartGame-function is being runned in the end
      
   - 2025-04-16 16.00 Worked for 1 hour
     - To make things easier for me I created new functions and variables to be able to check for check
       - I might change this back to the original idea to get shorter amount of code
     - 7 function
       - Copied the MovementManager and all the movement functions and changed their names
       - MovmentManager -> CheckManager
       - "Piece"Movement -> "Piece"Checker
     - 2 variables
       - kingslayer: replaced the chosenPiece variable in the new functions
       - checkSquares: an array that replaced the legalMoves variable in the new function. This stores all the enemie moves
     - Changed all the friendlyPieces variables to the enemyPieces variable and the other way around in the new movement functions
     - Shortened the PawnChecker
       - Removed the code for checking if the pawn could move forward, since it only can attack diagonally
       - Switched places on the code in the if(isWhiteTurn)
      
     - 2025-04-18 11.00 Worked for 1 hour
       - Changed the size of info1
         - For better visibility of what players turn it is
       - 1 button
         - upgradeButton: to confirm the choice of what piece to upgrade the pawns to
           - Pressing this goes to the UpgradePiece-function
       - 1 array
         - upgradePieces
           - Stores the pieces that the pawns can upgrade to
       - 6 functions
         - PieceInput
           - Updates infoText2 to ask the player what piece they wants to move
         - InvalidPiece
           - Updates infoText2 to tell the player that it is a invalid piece they have chosen
           - This function is being called if the player choses a piece that doesnt exist
         - NoLegalMoves
           - This function checks if the chosen piece can be moved
           - If not: infoText2 is being updated to tell this to the player
           - If the piece can be moved: the SquareInput-function is being called
         - SquareInput
           - Updates infoText2 to ask the player wich square they want to move the chosen piece
           - and hides the pieceButton and makes the squareButton visible
         - InvalidSquare
           - Updates infoText2 to inform the player they have chosen a square that the chosen piece cannot move to
         - CheckForUpgrade
           - Checks if a pawn has reached the end of the board
           - If it has: calls the UpgradePiece-finction
           - Else: calls the EndTurn-function
         - (these functions doesn't contain any new code, they where only created to make the buttons work and so infoText2 updates correctly)
    
