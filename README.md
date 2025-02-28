AutoTetris
 
AutoTetris is a Python project that includes an AI to play the classic game of Tetris. The AI evaluates the board state using several heuristics and decides the best move for the current tetrimino.
Directory Structure
 

autotetris/  
├── game.py  
├── game_defs.py  
├── tetris_ai.py  
├── high_score.txt  
├── README.md  
├── __pycache__/  
├── music/  
│   └── techno-tetris-theme.mp3  
└── without_ai/  
    ├── game.py  
    ├── high_score.txt  
    └── music/  
 

Files
 

game.py
 
This file contains the main game logic for Tetris, including board definition, collision detection, and matrix rotation.
game_defs.py
 
This file contains helper functions and constants used in the game, including board dimensions, matrix rotation, and collision checking.
tetris_ai.py
 
This file contains the AI implementation for Tetris, which uses various heuristics to evaluate the board state and determine the best move for the current tetrimino.
high_score.txt
 
This file stores the high score for the game.
music/
 
This directory contains music files used in the game.
without_ai/
 
This directory contains a version of the Tetris game without the AI implementation.
How to Run
 

Install Python 3.
Navigate to the project directory (autotetris).
Run the game with AI by executing: python game.py
Run the game without AI by navigating to the without_ai directory and executing: python game.py
AI Heuristics
 
The AI uses the following heuristics to evaluate the board state:
Aggregate Height: The sum of the height of each column.
Complete Lines: The number of complete lines on the board.
Holes: The number of empty spaces below a block in each column.
Bumpiness: The sum of the absolute differences in heights between adjacent columns.

These heuristics are combined using weights to compute a score for the board, which the AI uses to decide the best move for the current tetrimino. The weights can be adjusted to fine-tune the AI's performance.
