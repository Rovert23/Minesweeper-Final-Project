
Minesweeper Game Documentation
Introduction

This project is a Java implementation of Minesweeper game. The game is designed to be played in the console, and it allows the player to navigate a grid while avoiding mines and attempting to detect and mark them.
Game Objective

The objective of the Minesweeper game is to navigate through a grid and reveal all cells that do not contain mines, while avoiding hitting a mine. The player wins when a certain number of non-mine cells are revealed, and loses if they move over (hit) an undetectable mine.
Implementation Overview

The game's code is divided into several methods, each with a specific role:

    Initializing the Game Grid
        The initializeGrid method sets up the initial state of the game grid and fills each cell with brown square.

    Placing Mines
        The placeMines method randomly distributes mines across the grid. Some mines are detectable, while others are undetectable. The distribution ensures that mines are not placed in [0][0], [0][1], and [1][0] cells to ensure the player's safety.

    Printing the Game Grid
        The printGrid method displays the current state of the game grid in the console.

    Detecting Nearby Mines
        The detectNearbyMines method calculates the number of detectable and undetectable mines in the neighboring cells of a player's location. It also marks the detectable mines with a green checkmark and provides feedback about nearby mines.

    Main Method
        The program starts with the main method.

    Main Game Loop
        The game enters a loop that continues until the game is over.
        The main game loop in the main method handles player input, movement, and game progression. The player can use W, A, S, and D to move in different directions and Q to quit the game. The game loop also checks for winning and losing conditions.

    Mine Hit Check
        If the cell the player moves to contains an undetectable mine (undetectableMine), the game is over, and the player has lost. A "Game over!" message is displayed, and the grid is updated with fire emojis to indicate the mine explosion.

    Square Reveal and Winning Check
        If the cell the player moves to is a brown square, the detectNearbyMines method is called to reveal nearby mines, and the player wins a point.

    Winner Declaration
        If player points reach the winning points limit (15 points), the player wins. A "Congratulations! You won!" message is displayed, and the game is over.

    Method Invocations
        The methods initializeGrid, placeMines, printGrid, and detectNearbyMines are invoked as described above, are invoked from inside the main method.

    Game Symbols

    The game uses Unicode symbols to represent various elements:
        Brown Square: 🟫 (\uD83D\uDFEB)
        Green Checkmark: ✅ (\u2705)
        Fire: 🔥 (\uD83D\uDD25)
        Undetectable Mine: 🚨 (\uD83D\uDEA8)
        Detectable Mine: 💣 (\uD83D\uDCA3)

    Sample Grid

        Below is a sample of the grid prior to the player entering the game loop:

                                🟫🟫🟫🟫🚨🟫🟫🟫🟫🚨
                                🟫🚨🟫💣🟫🟫🟫🟫🟫🟫
                                🚨🟫🟫🟫🟫🟫🟫🟫🟫🟫
                                🟫🟫🟫🟫🟫💣🟫💣💣🟫
                                🟫🟫🟫🟫🟫💣🟫🟫🟫🟫
                                🟫🟫🟫🟫🟫🟫🟫🟫🟫🟫
                                💣🟫🟫🟫🟫🟫🟫💣🚨🚨
                                🟫🟫🟫🟫🟫🟫🟫💣🚨🟫
                                🟫🟫🟫🟫🚨💣🟫🟫🟫🟫
                                🟫🟫🟫🚨💣💣🟫🟫🟫🟫

        Here is a sample of gameplay, as well as a representation of the grid after the game concludes:

        W/A/S/D to move, Q to quit: d
        0 regular mine(s) were detected and swept nearby, but there's still 1 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: d
        0 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: s
        1 regular mine(s) were detected and swept nearby, but there's still 1 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: s
        0 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: d
        0 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: d
        0 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: d
        1 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: d
        0 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: s
        1 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: s
        1 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: s
        0 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: s
        1 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: s
        1 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: s
        1 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!
        W/A/S/D to move, Q to quit: s
        1 regular mine(s) were detected and swept nearby, but there's still 0 undetectable mine(s) nearby!

        Congratulations! You won!
        🟫🟫🟫🟫🚨🟫🟫🟫🟫🚨
        🟫🚨🟫✅🟫🟫🟫🟫🟫🟫
        🚨🟫🟫🟫🟫🟫🟫🟫🟫🟫
        🟫🟫🟫🟫🟫✅🟫✅💣🟫
        🟫🟫🟫🟫🟫✅🟫🟫🟫🟫
        🟫🟫🟫🟫🟫🟫🟫🟫🟫🟫
        💣🟫🟫🟫🟫🟫🟫✅🚨🚨
        🟫🟫🟫🟫🟫🟫🟫✅🚨🟫
        🟫🟫🟫🟫🚨✅🟫🟫🟫🟫
        🟫🟫🟫🚨💣✅🟫🟫🟫🟫

Game Rules

    The player starts at the top-left corner of the grid.
    The player can move in four directions: up (W), left (A), down (S), and right (D).
    If the player attempts to move in a direction that would lead them outside of the grid bounds, the game mechanism should keep the player in their current location in that case.
    The player can reveal cells by moving over them, marking cells with detectable mines, and detecting nearby mines.
    The player wins when a certain number of non-mine cells are revealed.
    The player loses if they hit an undetectable mine.
    The player can quit the game at any time by pressing 'Q'.

Evaluation Criteria

    Functionality:
        Does the game function correctly without any major bugs or crashes?
        Can the player move within the grid, reveal squares, and mark mines as intended?
        Are game rules (winning and losing conditions) correctly implemented?

    User Interface:
        Is the game interface user-friendly and intuitive?
        Are the instructions clear and concise?
        Is the game visually appealing and well-formatted for the console?

    Customization:
        Can the grid size and the number of mines be easily customized?

    Randomization:
        Are mines distributed randomly across the grid, ensuring a different game experience with each playthrough?
        Is there a mechanism to prevent initial placement of mines in certain cells (e.g., [0, 0], [0, 1], and [1, 0])?

    Code Quality:
        Is the code well-structured and organized with clear functions and meaningful variable names?
        Are comments and documentation provided to explain the purpose and functionality of the code?
        Does the code follow good programming practices, such as DRY (Don't Repeat Yourself)?

    Game Progression:
        Does the game progress logically, from the player's input to winning or losing conditions, and ultimately to game over?

    Testing and Verification:
        Has the project been tested thoroughly to ensure that it functions as expected in various scenarios?
        Is the game reliable and stable during gameplay?

    Creativity and Additional Features (Optional):
        Did the developer incorporate any additional features or creative elements to enhance the game experience?

    Usability:
        Is the game enjoyable to play, and does it provide an engaging user experience?

Submission and Demonstration

    The project must be submitted on Canvas by the deadline, which is midnight on December 4th (FIRM DEADLINE). Failure to do so will result in a score of 0 for this project.
    Students should demonstrate their submitted projects on December 5th during class sessions. If some groups can't demo their project during the class sessions, they will have to do it during the office hours on the same day. Failure to do so will result in a score of 0 for this project.
    Teams will demo their project according to their orders in the project teams list on Canvas.
    During the demonstration, all team members will be asked questions to assess their understanding of the concepts used and the flow of the code.

Learning Outcomes

This Minesweeper game project is an interactive console-based implementation that provides a fun and challenging gaming experience. It demonstrates the use of arrays, randomization, and control structures, and methods in Java. Students can learn and practice their programming skills while enjoying the game. Have fun playing and learning!
