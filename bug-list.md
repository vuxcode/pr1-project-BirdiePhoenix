# Bug List

> Make a list of the things that don't work as expected. Keep a list of things that you have fixed and try to document how you solved them.

1. Problem: The whole board was not printed and the white pieces didn't show. The problem was that I had written 2 too many *empty* rows so that the white ones was missed out during the printing process.
2. Problem: I had written pieceIndex.includes() instead of choosenPiece.includes() so the pawn functions couldn't be called on.
3. Problem: Everything inside the unMovedPawns array was deleted. In the PawnMovement function I had only written unMovedPawns.splice(coosenPiece), it was solved when I added ", 1" after the variable.
4. Problem: Elements was removed from the unmovedPawns array even when the pawn had already been moved and removed from the array.
   Solution: Added an if-statement so an element only removes when the chosen piece is still inside the array.
5. Problem: The rooks and the pawns where able to take pieces of the same color
   Solution: Check if there is a piece of the same color on the square
6. Problem: If the rooks where on the top or bottom rows it said that the blackPieces array was not defined
   Solution: I added that the program should check if the piece where on the top or bottom line in the "break" if-statement
7. Problem: The white rooks could move like the black pieces. I had just copied the black movement and only changed the numbers.
   Solution: I changed all the instances of whitePieces to blackPieces and all the instances of blackPieces to whitePieces
8. Problem: In the BishopMovement- and RookMovement-functions the while-loops added squares to the legalMoves-array above or under the squareNames index range.
   Solution: Made the while-loops check if possibleMoves +/- x is larger than 0 or smaller than 63
9. Problem: When changing the chosenPiece-variable into the pieceVar-variable bugs appeard becaus i didn't change it on all places needed
10. Problem: A lot of bugs when I tried to replace the prompts and alerts with html.
    Solution: Had to go back to the last saved version.
11. Problem: Runned into some bugs when adding the textbox
    Solution: I hade to create some new functions and rearrange what some of the function does so it could work with the textbox and the buttons
12. Problem: When you don't write anything when pressing "Confirm Piece" there is following error: Maximum Call stack size exceeded.
    Solution: I havn't done anything to solve this yet since it doesn't break the program
13. Problem: a lot of bugs appeard when implementing the check functions.
    Solution The checkStorage didnt update properly so error occured
14. Problem: The king could move to a square where it would be in check
    Solution: Inside EnemyCheckChecker, replaced chessBoard with checkStorage in the condition for the if-statement
15. Problem: The player became check mate instead of just check
    Solution: Changed the i-variables in the for-loops in MateChecker and EnemyCheckChecker so they are not the same
16. Problem: The players could move pieces or not move pieces that was not supposed to or supposed to be moved when in check
    Solution: When resetting the checkStorage array I had written that the square where the enemy pieces had been moved to during the checking for check was gonna be "[]" which brakes the program if that square contained a friendly piece. Replaced "[]" with chessBoard[possibleMoves]
17. Problem: The check mechanics didn't quite work as it should
    Solution: I created the wouldBeCheck variable so that the isCheck wasn't turned false when it shouldn't be
18. Problem: The next player was asked for castling when previously player pressed no on the question
    Solution: Added so all isCastling... is being turned false in PieceInput() since the correct ones is turned false in CheckingForCastling() in TurnOrder()
19. Problem: When upgrading a pawn to a piece where number 1 had been taken it became number 2 so there was two number 2.
    Solution: Added two arrays that also stores the different pieces since the poeces in blackPieces and whitePieces gets removed when taken
20. Problem: If a pawn took a piece behind an enemy pawn the enemy pawn disapeard
    Solution: Added so enPassantSquare = "" in EndTurn().
