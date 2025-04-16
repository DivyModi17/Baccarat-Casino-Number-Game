# Baccarat Game (CLI Version)

![Baccarat](https://your-baccarat-image-url.com)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Code Breakdown](#code-breakdown)
- [Contributing](#contributing)
- [License](#license)

## Overview
This is a console-based Baccarat game developed in C++ by Kevin Villania. The game simulates a virtual casino where a player can bet on either the banker or player, and cards are drawn to determine the winner based on the Baccarat rules. The game is played with numeric cards (1–10) and the goal is to get a sum closest to 9.

## Features
- Fully functional CLI-based Baccarat game
- Player can bet on either Banker or Player
- Automatic calculation of winner based on Baccarat rules
- Random card generation simulating a shuffled deck
- Support for replays and session money tracking

## Installation
### Prerequisites
- C++ Compiler (like g++)
- Windows Command Line or compatible terminal

### Compilation
```bash
g++ baccarat_game.cpp -o baccarat_game.exe
```

### Running the Game
```bash
./baccarat_game.exe
```

## Usage
- Enter your name to begin.
- Choose to bet on BANKER (1) or PLAYER (2).
- Enter a bet amount.
- View the drawn cards and determine the result.
- Play again or exit based on your choice.

## Code Breakdown
### 1. Struct Declaration
```cpp
struct Number {
    int num1, num2, sum, extraCard;
};
```
Holds the details for two main cards, their sum, and an optional third card if needed.

### 2. Main Function
Initializes the game, handles input/output, and loops through the game round-by-round until the user quits or runs out of money.

### 3. Card Drawing Logic
```cpp
banker.num1 = rand() % 10 + 1;
banker.num2 = rand() % 10 + 1;
banker.sum = (banker.num1 + banker.num2) % 10;
```
Simulates two card draws and checks for a natural win (8 or 9). If not a natural win, an extra card is drawn and added.

### 4. Display Functions
```cpp
void printCard1(...)
void printCard2(...)
```
- `printCard1` shows three cards including extra.
- `printCard2` is used if the hand is a natural win and shows only two cards.

### 5. Game Result Evaluation
```cpp
int winnerFunction(int bankerCard, int playerCard);
```
- Compares totals and returns 1 (Banker), 2 (Player), or 3 (Draw).

### 6. Score Calculation
```cpp
int declareWinner(...);
```
- Evaluates the bet and updates player balance based on the winner.

### 7. Play Again Logic
```cpp
bool playAgain(...);
```
- Returns `true` or `false` based on player's input and remaining money.

## Contributing
To contribute:
1. Fork this repository
2. Make changes in a new branch
3. Create a Pull Request with a detailed description

## License
This project is licensed under the MIT License.

---
### Presentation Tips for Students
- **Purpose:** Showcase your understanding of control structures, randomness, and function-driven design in C++.
- **Highlight Concepts:** Emphasize card logic, random number generation, and input validation.
- **Interactively Demo:** Let the professor or peers interact with the game during demo time.

---

> Developed by **Kevin Villania**
> Contact: villaniakevin07@gmail.com
