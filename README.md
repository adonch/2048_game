# 2048 Game

A fully playable implementation of the classic [2048 puzzle game](https://play2048.co/), built with vanilla JavaScript as part of my frontend development portfolio.

## 🎮 Demo

[Play the game →](https://adonch.github.io/2048_game/)

## About

2048 is a sliding tile puzzle where you combine numbered tiles on a 4×4 grid. Slide in any direction to merge tiles of equal value — keep going until you reach **2048**, or until the board fills up with no moves left.

This project focuses on clean game logic separated from UI rendering, with a `Game` class that manages all state independently from the DOM.

## Features

- Full 4×4 grid gameplay with keyboard arrow controls
- Tile merging logic — equal tiles combine, merged tiles can't merge again in the same move
- Score tracking — increases by the sum of all merged tiles per move
- Random tile spawning after each move (2 with 90% probability, 4 with 10%)
- Win detection at 2048, game-over detection when no moves remain
- Start / Restart button with state reset
- Clean separation of game logic (`Game` class) and UI layer

## Tech Stack

- Vanilla JavaScript (ES6 classes)
- HTML5 / CSS3
- No external libraries or frameworks

## Getting Started

```bash
git clone https://github.com/adonch/2048_game.git
cd 2048_game
npm install
npm start
```

Open `http://localhost:8080` in your browser.

## Project Structure

```
src/
├── modules/
│   └── Game.class.js   # Core game logic
├── index.html          # Game UI
├── main.js             # UI wiring — uses Game class instance
└── styles/
    └── main.scss
```

## Game class API

The `Game` class in `src/modules/Game.class.js` is the heart of the project. It manages all game state with no DOM dependencies.

| Method | Description |
|---|---|
| `new Game(initialState?)` | Creates a new game; optional initial board state |
| `getState()` | Returns the current 4×4 board as a 2D array |
| `getScore()` | Returns the current score |
| `getStatus()` | Returns `'idle'`, `'playing'`, `'win'`, or `'lose'` |
| `start()` | Starts the game with two initial tiles |
| `restart()` | Resets board, score, and status |
| `moveLeft()` | Slides and merges tiles left |
| `moveRight()` | Slides and merges tiles right |
| `moveUp()` | Slides and merges tiles up |
| `moveDown()` | Slides and merges tiles down |

## How to Play

- Use the **arrow keys** to slide all tiles in a direction
- Two tiles with the same number **merge into one** with double the value
- A new tile (**2** or **4**) appears after each valid move
- Reach **2048** to win — or keep going for a higher score!
- The game ends when no valid moves remain

## License

MIT

## Author
Anton Donchenko - Fullstack developer
- [Author](https://github.com/adonch)
- [LinkedIn](https://www.linkedin.com/in/anton-donchenko-83aa85165/)
- Email: donch.a080@gmail.com

