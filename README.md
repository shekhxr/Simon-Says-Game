# Simon Says Game

This is a web-based implementation of the classic memory game "Simon Says." The game challenges players to remember and repeat a sequence of colors.

## Features

* **Interactive Gameplay:** Users press keys to start the game and click on colored buttons to follow the sequence.
* **Level Progression:** The game increases in difficulty with each successful round by adding another color to the sequence.
* **Visual Feedback:** Buttons "flash" to indicate the computer's sequence and the user's clicks.
* **Game Over Screen:** Notifies the player of their score when they make a mistake.
* **Reset Functionality:** Allows players to easily restart the game after it ends.

## Technologies Used

* HTML5
* CSS3
* JavaScript

## How to Play

1.  **Start the Game:** Open the `index.html` file in your web browser. Press any key on your keyboard to begin.
2.  **Watch the Sequence:** The game will flash a sequence of colors.
3.  **Repeat the Sequence:** Click the colored buttons in the same order as they were flashed.
4.  **Level Up:** If you successfully repeat the sequence, the game will advance to the next level, and a new color will be added to the sequence.
5.  **Game Over:** If you click the wrong color, the game will end, and your score (the level you reached) will be displayed.
6.  **Restart:** Press any key to start a new game.

## Project Structure

* `index.html`: The main HTML file that structures the game's interface.
* `style.css`: Contains the CSS rules for styling the game elements.
* `app.js`: Implements the game logic, including sequence generation, user input handling, and game state management.

## Setup

1.  Clone this repository to your local machine or download the files.
2.  Open the `index.html` file in your preferred web browser.

## Code Overview

### `app.js`

* `gameSeq`: An array to store the computer's sequence of colors.
* `userSeq`: An array to store the user's entered sequence of colors.
* `btns`: An array containing the available button colors.
* `started`: A boolean flag to track if the game has begun.
* `level`: An integer representing the current game level.
* `document.addEventListener("keypress", ...)`: Initiates the game when any key is pressed.
* `gameFlash(btn)`: Adds and removes a "flash" class to visually indicate the computer's turn.
* `userFlash(btn)`: Adds and removes a "userflash" class to visually indicate the user's click.
* `levelUp()`: Increments the level, clears the user's sequence, generates a new random color for the game sequence, and triggers `gameFlash`.
* `checkAns(idx)`: Compares the user's input with the game sequence and handles game progression or game over conditions.
* `btnPress()`: Handles user button clicks, records the user's color, and calls `checkAns`.
* `allBtns`: Selects all game buttons and attaches a `click` event listener to each.
* `reset()`: Resets all game variables to their initial state for a new game.
