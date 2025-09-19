# Tic Tac Toe

> A small, well-structured Tic Tac Toe project with two implementations:
>
> 1. **C++ Console** — Object-oriented design using Strategy/Observer/Factory patterns (`TicTacToe.cpp`)  
> 2. **Web Frontend** — Simple browser playable version using HTML/CSS/Vanilla JS (`index.html`, `style.css`, `app.js`)

---

## Demo

- **Web version:** Open `index.html` in a browser and play a 3×3 Tic Tac Toe.
- **C++ console version:** Play a customizable NxN Tic Tac Toe in terminal.

---

## Table of Contents

- [Features](#features)  
- [Architecture & Design](#architecture--design)  
- [Run / Install](#run--install)  
  - [Web (Browser)](#web-browser)  
  - [C++ (Console)](#c-console)  
- [Files & Structure](#files--structure)  
- [Design Patterns Used](#design-patterns-used)  
- [How to Play](#how-to-play)  
- [Examples / Sample Output](#examples--sample-output)  
- [Tests & Roadmap](#tests--roadmap)  
- [Contributing](#contributing)  
- [License & Credits](#license--credits)

---

## Features

- Two implementations:
  - **C++ (OOP)**: modular classes for `Game`, `Board`, `Player`, `Symbol`, `Rules`, observer for notifications and a factory for creating games.
  - **Web (JS)**: interactive UI, click boxes, winner detection, draw detection, reset & new game.
- Supports NxN board in C++ (user chooses board size at start).
- Clean separation of concerns and easy to extend (e.g., add new rules or AI).
- Uses common software patterns (Strategy for rules, Observer for notifications, Factory for game creation).

---

## Architecture & Design

The C++ implementation follows an object-oriented design. Key classes (see `UML.jpeg`):

- `TicTacToeGame` — orchestrates players, rules, board, and observers
- `Board` — grid management, placement, display
- `TicTacToePlayer` — stores player info (id, name, symbol, score)
- `Symbol` — mark used by a player (e.g., 'X' or 'O')
- `TicTacToeRules` (abstract) — defines rules interface
  - `StandardTicTacToeRules` — concrete implementation for standard rules
- `IObserver` (abstract) — Observer interface (e.g., `ConsoleNotifier`)
- `TicTacToeGameFactory` — Factory class to create games

This design makes it easy to:
- Swap different rule sets (e.g., custom win conditions)
- Plug in different notifiers (UI update, network notification)
- Extend to AI players or network multiplayer

---

## Run / Install

### Web (Browser)
1. Clone the repo or download files.
2. Open `index.html` in your browser (Chrome/Firefox).
3. Play by clicking boxes. Use **Reset Game** or **New Game** to restart.

