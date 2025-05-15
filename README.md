[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/zon3mdIg)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=18870410&assignment_repo_type=AssignmentRepo)
# Project Instructions
Follow the instructions here: https://vuxcode.netlify.app/new/pr1/lessons/major-project-brief/

REMEMBER TO "COMMIT" YOUR CHANGES REGULARLY TO SHOW HOW YOU HAVE BUILT THIS PROJECT! 

The final program is not the goal! The aim of the project is to show how you have developed your program, the steps you have taken and the problems you have solved!

# Project Notes

- Checkmechanics:
  - King-movement
  - Different movement manager when in check
- Rouqade
- Pawn take 2 moves next to pawn
- Fix upgrade

- Buttons if time    

# Project Summary
- Presentation
  - A chess game

- Improvements:
  - The main thing to improve if I had more time would be the visuals of the game. Instead of having a HTML based game it would be a much better experience for the players if their was an actual board on the screen, with pieces you could move by dragging them or pushing them and the squares. To be able to this I would need much more knowledge in webbutveckling and HTML code.
  - Another thing to improve would be to show on the screen all the square names. This is probably something I could have figured out, without any further knowledge, but the only way I could think of right now is to include those in the array which would mean I had to change the loops, so they don't check those elements.
  - It would also be nice to highlight the squares where you could move to, which could be made by changing the color of those elements
  - The pawn functions could also be changed into using loops to calculate the moves. For this to work I would have to create a variable that can be used to distinguish the differnet player colours.

- Budget:
  - The total amount of hours spent on the project: 76 hours
  - The main reason for this was the change to 2D arrays
    - In the conversion I spent about 20 hours only fixing the bugs that appeard, mainly on check bugs
  - After about 35 hours I had implemented everything that I promised to include, except for the pickups since I chose to not include any pickups
  - If I, from the beginning, had made the arrays in 2D, I could probably have made the project in about 30 hours, that is if you don't include the problems below
  - The main reasons why I excided the 30 hours (except for the 2D-conversion) was the following:
1. Bug-fixes:
  - Quite alot of bugs appeard during the developement, some appeard when solving curtain things like the check mechanics, but some where due to sloppy mistakes
2. Learned new things:
  - For example how to create textboxes
    - Before that, I used alerts and prompts to build the game, it took some hours to convert it to the new system (textbox and buttons)
3. Poor planning
  - Even though my planning wasn't super bad, it could have been alot better
  - I should have really thought about the mechanics that the program would need, and exactly what those mechanics would need to be able to work

# User Guide
How To Play:

Uppercase is the black pieces and lowercase is the white pieces.
P = Pawn,
R = Rook,
N = Knight,
B = Bishop,
Q = Queen,
KI = King.

1. Press Start Game
2. Write what piece you want to move. (use the letter of the piece and the number to speciefy which of those pieces you want to move)
3. Press Confirm Piece
4. Write what square you want to move the piece to. (A-H + 1-8)
5. Press Confirm Square
6. If Castling is possible;
   -Press Yes or No
   -Press what rook you want to use in the Castling (r1. r2, R1, R2)
7. When reaching the edge of the board with a pawn, you may upgrade it
   -Write what kind of piece you want to upgrade the pawn into.
     R = Rook,
     N = Knight,
     B = Bishop,
     Q = Queen.
8. When a player is in Check Mate, press Restart Game if you want to play again

