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
8. Problem: In the BishopMovement-function the while-loops added squares to the legalMoves-array above or under the squareNames index range.
   Solution: Made the while-loops check if possibleMoves +/- x is larger than 0 or smaller than 63
