# Mini-Game-Project-Tic-Tac-Toe-Snake-Game-
To create a console-based mini game in C++ that demonstrates core programming concepts such as loops, arrays, and conditional logic.
## 2. Users and Usage Scenarios

**Target Users**: General web users seeking casual gaming entertainment

**Core Usage Scenarios**:
- Users want to play Tic Tac Toe with another player locally
- Users want to play Snake Game solo for score challenge
- Users want to replay games after completion

## 3. Page Structure and Functionality

### Page Hierarchy

```
Mini Game Collection
├── Game Selection Screen
├── Tic Tac Toe Game Screen
└── Snake Game Screen
```

### 3.1 Game Selection Screen

**Purpose**: Allow users to choose which game to play

**Functionality**:
- Display application title
- Display two game options: Tic Tac Toe and Snake Game
- User clicks on a game option to enter corresponding game screen

### 3.2 Tic Tac Toe Game Screen

**Purpose**: Provide 2-player local Tic Tac Toe gameplay

**Functionality**:
- Display 3x3 game board
- Display current player indicator (Player X or Player O)
- Player clicks empty cell to place their mark
- Board updates dynamically after each move
- Display move history showing sequence of moves
- Detect and announce win condition when three marks align horizontally, vertically, or diagonally
- Detect and announce draw condition when board is full with no winner
- Display replay button after game ends
- Display return to game selection button

### 3.3 Snake Game Screen

**Purpose**: Provide single-player Snake Game gameplay

**Functionality**:
- Display game board with snake and food
- Display current score
- Display current level
- User controls snake direction using keyboard arrow keys
- Snake moves continuously in current direction
- Board updates dynamically after each tick
- Snake grows when eating food
- New food appears at random position after being eaten
- Score increases when snake eats food
- Level increases based on score milestones
- Detect and announce loss condition when snake collides with wall or itself
- Display replay button after game ends
- Display return to game selection button

## 4. Game Rules and Logic

### 4.1 Tic Tac Toe Rules

**Turn System**:
- Player X always starts first
- Players alternate turns
- Each player places one mark per turn

**Win Conditions**:
- Three marks in a row horizontally
- Three marks in a column vertically
- Three marks diagonally (top-left to bottom-right or top-right to bottom-left)

**Draw Condition**:
- All 9 cells filled with no win condition met

**Move History**:
- Record each move with player identifier and cell position
- Display moves in chronological order

### 4.2 Snake Game Rules

**Movement**:
- Snake moves continuously in current direction
- Direction changes when user presses arrow key
- Snake cannot reverse direction (e.g., cannot go left if moving right)

**Food Mechanics**:
- One food item appears on board at a time
- Food appears at random empty position
- Snake grows by one segment when eating food
- New food appears immediately after current food is eaten

**Scoring**:
- Score increases by 10 points per food eaten

**Level Progression**:
- Level 1: 0-49 points
- Level 2: 50-99 points
- Level 3: 100-149 points
- Level increases every 50 points
- Snake speed increases with each level

**Loss Conditions**:
- Snake head collides with any wall boundary
- Snake head collides with any part of its own body

**Replay**:
- Reset score to 0
- Reset level to 1
- Reset snake to initial position and length
- Reset snake speed to level 1 speed

## 5. Exception and Boundary Cases

| Scenario | Handling |
|----------|----------|
| User clicks occupied cell in Tic Tac Toe | No action, turn does not change |
| User presses multiple arrow keys rapidly in Snake Game | Only process most recent valid direction change |
| Snake grows to fill entire board | Continue game, food cannot appear |
| User navigates away during game | Game state is lost, restart from beginning |

## 6. Acceptance Criteria

1. User opens application and sees Game Selection Screen with two game options
2. User clicks Tic Tac Toe option and enters Tic Tac Toe Game Screen
3. User plays complete Tic Tac Toe game with another player until win or draw is detected
4. User clicks replay button and starts new Tic Tac Toe game
5. User returns to Game Selection Screen
6. User clicks Snake Game option and enters Snake Game Screen
7. User plays Snake Game, eats food, increases score and level
8. Game detects loss condition when snake collides with wall or itself
9. User clicks replay button and starts new Snake Game

## 7. Out of Scope for Current Release

- Single-player mode with AI opponent for Tic Tac Toe
- Online multiplayer functionality
- Leaderboard or score persistence
- Additional game modes or difficulty settings
- Sound effects or background music
- Pause functionality for Snake Game
- Customizable board size or snake speed
- Mobile touch controls optimization
- Game state saving or resume functionality
