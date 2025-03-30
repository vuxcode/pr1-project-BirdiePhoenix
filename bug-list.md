# Bug List

> Make a list of the things that don't work as expected. Keep a list of things that you have fixed and try to document how you solved them.

1. Problem: The whole board was not printed and the white pieces didn't show. The problem was that I had written 2 too many *empty* rows so that the white ones was missed out during the printing process.
2. Problem: I had written pieceIndex.includes() instead of choosenPiece.includes() so the pawn functions couldn't be called on.
3. Problem: Everything inside the unMovedPawns array was deleted. In the PawnMovement function I had only written unMovedPawns.splice(coosenPiece), it was solved when I added ", 1" after the variable.
4. Problem: Elements was removed from the unmovedPawns array even when the pawn had already been moved and removed from the array.
   Solution: Added an if-statement so an element only removes when the chosen piece is still inside the array.
