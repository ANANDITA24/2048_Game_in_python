# 2048_Game_in_python

This code implements a playable version of the 2048 game in Python using the Tkinter library. Here's a breakdown of the code:

**Libraries:**

* `tkinter`: Used for creating the graphical user interface (GUI) elements.
* `random`: Used for generating random numbers for tile placement.

**Class: `Play_2048`**

This class is the core of the game. It inherits from `Tk` and defines the functionalities of the game:

* **Class Variables:**
    * `game_board`: A 2D list representing the game board with numbers.
    * `new_random_tiles`: A list of possible values for new tiles (e.g., 2, 4).
    * `score`: Stores the current game score.
    * `high_score`: Stores the highest achieved score.
* **__init__ method:**
    * Initializes the game window with title "2048 GAME" and sets minimum size.
    * Creates UI elements like buttons and labels for score and record.
    * Initializes the canvas for drawing the game board.
    * Calls the `new_game` method to start a new game.
* **new_tiles method:**
    * Randomly selects a new tile value from `new_random_tiles`.
    * Finds an empty spot on the board and places the new tile.
    * Draws the new tile on the canvas.
* **full method:**
    * Checks if all cells on the board are filled (no empty spaces).
* **show_board method:**
    * Iterates through the game board and displays each cell based on its value.
    * Uses different colors and fonts for different tile values.
* **moves method:**
    * Captures user key presses (arrow keys).
    * Moves the tiles in the specified direction (up, down, left, right).
    * Merges adjacent tiles with the same value when possible (doubles the value).
    * Updates the score and checks for game over or win conditions.
    * Calls `new_tiles` and `show_board` to update the board after each move.
* **new_game method:**
    * Resets the score and game board.
    * Places two random tiles (2 or 4) on the board.
    * Calls `show_board` to display the initial board.
* **game_over method:**
    * Checks for win condition (a tile with value 2048) and displays a "YOU WON!" message.
    * Checks for lose condition (no empty spaces and no possible merges) and displays a "GAME OVER" message.
* **game_won method:**
    * Displays a "YOU WON!" message on the canvas.

**Main Execution:**

* The `if __name__ == "__main__":` block ensures the code within only executes when the script is run directly (not imported as a module).
* It creates an instance of the `Play_2048` class.
* Binds the `moves` method to all key presses, enabling user interaction.
* Starts the main event loop (`mainloop`) to keep the window running and responsive.
