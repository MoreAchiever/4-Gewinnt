# 🎮 Connect Four — Canvas Game

Bonus Homework — *Informatik I*

This project implements a simplified **Connect Four** game using a custom programming language syntax with canvas-based rendering. Two players (Red and Blue) take turns placing their tokens on a grid, aiming to connect four in a row — horizontally, vertically, or diagonally.

## 📌 Features

- Variable-sized game board (3x3 to 9x9)
- Canvas-based visual representation
- Keyboard interaction (keys 1–9 to play)
- Win detection for:
  - Horizontal lines
  - Vertical lines
  - Ascending diagonals (`/`)
  - Descending diagonals (`\`)
- Player switch logic
- Game end detection (winner or full board)

## 🧠 Concepts Used

- Object-oriented programming (class `Gamemap`)
- Matrix (2D vector) manipulation
- Canvas drawing (circles and text)
- Event-driven programming (keyboard input)
- Basic algorithmic checks for winning conditions

## 🧱 Structure

### Main Components

#### `Gamemap` Class

Manages the game logic and state.

| Method | Description |
|--------|-------------|
| `constructor(ha, va)` | Initializes board with given dimensions |
| `assignVector()` | Creates a 2D array filled with zeros |
| `play(column)` | Places a token in a given column |
| `set_GameVector(row, col)` | Sets the value at a specific location (Red/Blue) |
| `assendVector()` | Creates a diagonal matrix for `/` direction |
| `descendVector()` | Creates a diagonal matrix for `\` direction |
| `representiereSplaten()` | Labels each column visually |
| `get_*()` methods | Accessors for board vectors and dimensions |

#### `Representation(g_map)`
Draws the current game state on the canvas.

#### `checkWinner(g_map)`
Evaluates the board for a win in all directions.

#### `checkPlayable(g_map)`
Checks if there are any moves left.

#### `PrintWinner(winner)`
Displays the winner message on the screen.

#### `whoWon(color)`
Sets the global `winner` variable.

## 🕹️ How to Play

1. The board appears on screen.
2. Use keys **1** to **7** (or up to the column size) to place your token.
3. Red and Blue alternate turns.
4. The game ends when a player wins or the board is full.

## 🧪 Example Game

```js
var x = Gamemap(7, 7);
Representation(x);
setEventHandler("canvas.keydown", function(event){
	// Interact using keyboard numbers
});
enterEventMode();
```

## 📚 Notes

- The game asserts that both rows and columns are between 3 and 9.
- Uses `use namespace canvas;` and `use namespace math;`.
- The code is written in a pseudo-JavaScript-like custom language for educational use.

## 🏁 Result

A fully interactive Connect Four game running in a canvas with clear visual feedback and functional gameplay!
