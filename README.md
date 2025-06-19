<u> Tic Tac Toe </u>
 
<br>
This is a simple web-based Tic Tac Toe game built with three files: index.html, style.css, and script.js. The HTML file sets up the page structure (a heading, a 3×3 game board, a turn indicator, and a reset button). The CSS file provides the styling for layout, colors, and hover effects. The JavaScript file contains the game logic and handles user interactions like placing marks, checking for a win or draw, and resetting the board.

File Overview

•	index.html: Defines the page structure and elements. It includes a container with a title, a 3×3 grid (.board) of clickable cells (.cell), a paragraph to show whose turn it is (#turn), and a “Reset” button. Each cell has an onclick handler that calls the placeMark(index) function with its position (0–8). The HTML also links to style.css for styling and script.js for game logic.

•	style.css: Styles the game’s appearance. The body is centered with a dark background. The .board is a 3×3 grid with evenly sized cells. Each .cell has a base color, border, and a hover effect that lightens the background and slightly scales up the cell. Pseudo-classes (.cell.X::after and .cell.O::after) are defined to display “X” in red or “O” in blue when those classes are applied to a cell. The “Reset” button and turn display (#turn) are also styled (colors, padding, hover effects).

•	script.js: Implements the game logic. It tracks the current player (currentPlayer), the board state (an array of 9 strings), and whether the game is active. The key functions are:
•	placeMark(index): Called when a cell is clicked. If the game is active and the chosen cell is empty, it records the current player’s mark in the board array and updates that cell’s display. It then checks for a win or a draw. If a win is found, it updates the turn display to announce the winner and stops the game. If the board is full without a winner, it declares a draw. Otherwise, it switches the currentPlayer (X → O or O → X) and updates the turn message.
•	checkWin(): Checks all winning combinations of indices to see if any three cells in a row belong to the same player. Returns true if there is a win.
•	checkDraw(): Checks if all cells are filled (no empty strings left) and there is no winner, indicating a draw.
•	resetBoard(): Resets the game to the initial state by clearing the board array and the cell displays, setting currentPlayer back to “X,” reactivating the game, and updating the turn message to start a new round.

Game Flow

1.	Start: The game initializes with currentPlayer = 'X' and an empty board. The turn indicator shows “Player X’s turn.”
2.	Player Move: When a player clicks an empty cell, placeMark(index) runs. It updates the board state and the clicked cell’s content to “X” or “O.”
3.	Check Win/Draw: After each move, the code checks for a winning combination. If found, it displays “Player X wins!” or “Player O wins!” and stops further moves. If all cells are filled with no winner, it displays “It’s a draw!”.
4.	Switch Turns: If the game is still active (no win or draw), the code switches currentPlayer to the other player and updates the turn text (e.g., “Player O’s turn”).
5.	Reset: Clicking the Reset button clears the board, resets the turn to “Player X,” and allows a new game to start.
   
User Interface Behavior

•	Layout and Style: The board is a centered 3×3 grid with dark-themed colors. Cells are large squares (100×100px) with a subtle shadow and border.
•	Hover Effects: Moving the mouse over a cell slightly lightens its color and scales it up, giving interactive feedback before clicking. The Reset button also changes color on hover.
•	Displaying Marks: When a player clicks a cell, an “X” or “O” appears in that cell. In the intended design, “X” marks are colored red and “O” marks are colored blue (using CSS pseudo-elements). The turn indicator text above the button shows which player’s move is next.
•	Dynamic Updates: After each move, the script updates the board visually and updates the turn indicator. When the game ends, the turn indicator changes to either “Player X wins!,” “Player O wins!,” or “It’s a draw!” without allowing further clicks. The Reset button clears these changes to start over.

Overall, the three files work together to create a simple interactive Tic Tac Toe game: the HTML provides the structure, the CSS makes it look polished and interactive, and the JavaScript handles all the gameplay rules and updates.

