**Project Title**

Tic-Tac-Toe AI Player

---

## Overview

This project implements a Tic-Tac-Toe game with an AI opponent using the Minimax algorithm. The project consists of two primary Python files:

* `tictactoe.py`: Contains all game logic and AI functions.
* `runner.py`: Provides a simple graphical interface for playing the game against the AI.

When complete, you can run the game with:

```bash
python runner.py
```


## Dependencies

* Python 3.6+
* `pygame` (for the graphical interface in `runner.py`)

Install dependencies with:

```bash
pip install pygame
```

---

## Usage

1. Ensure all dependencies are installed.
2. From the project root, run:

   ```bash
   python runner.py
   ```
3. The Tic-Tac-Toe window will appear. Play against the AI by clicking on cells.

---

## Game Logic (`tictactoe.py`)

The game board is represented as a 3×3 grid, implemented as a list of three lists. Each cell can take one of three values:

* `X`: Player X's move
* `O`: Player O's move
* `EMPTY`: An empty cell

Key functions implemented:

* `initial_state()`: Returns the starting empty board.
* `player(board)`: Returns which player's turn it is (`X` or `O`).
* `actions(board)`: Returns the set of all possible moves on the board.
* `result(board, action)`: Returns the board that results from making a move.
* `winner(board)`: Returns the winner of the game (`X`, `O`, or `None`).
* `terminal(board)`: Determines if the game is over.
* `utility(board)`: Returns the utility value of a terminal board (`1` for X win, `-1` for O win, `0` for draw).
* `minimax(board)`: Implements the Minimax algorithm to determine the optimal move for the current player.

---

## AI Strategy

The AI uses the Minimax algorithm:

1. Recursively explore all possible game states.
2. Evaluate terminal states with the utility function.
3. Backpropagate optimal choices for each player, assuming both play optimally.

This ensures the AI never loses and forces a draw at worst.

