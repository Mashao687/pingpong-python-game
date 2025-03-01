# Pong Game using Pygame

## Description
This is a simple Pong game built using Pygame. The game involves two players controlling paddles to hit the ball back and forth. If the ball passes behind a player's paddle, the opponent wins the round. The game runs until the window is closed.

## Prerequisites
Before running this game, ensure that you have Python and Pygame installed on your system.

### Installing Python
If you do not have Python installed, download and install it from [Python's official website](https://www.python.org/).

### Installing Pygame
To install Pygame, open a terminal or command prompt and run:
```bash
pip install pygame
```

## Image Files Used
This game requires two image files:
1. `block.png` - Represents the paddles controlled by the players.
2. `tennis.png` - Represents the ball in the game.

### Connecting Image Files to the Code
- The `GameSprite` class loads an image file and scales it to the required size using:
  ```python
  self.image = transform.scale(image.load(player_image), (weight, height))
  ```
- The `Player` class inherits from `GameSprite` to create paddles (`racket1` and `racket2`) using:
  ```python
  racket1 = Player('block.png', 30, 200, 4, 50, 150)
  racket2 = Player('block.png', 520, 200, 4, 50, 150)
  ```
- The ball is created using:
  ```python
  ball = GameSprite('tennis.png', 200, 200, 4, 50, 50)
  ```
- Ensure that `block.png` and `tennis.png` are in the same directory as the Python script.

## How to Run the Game in VS Code
1. **Open the project in VS Code**
   - Open VS Code and navigate to the folder containing the script.
   - Ensure that the required image files (`block.png` and `tennis.png`) are in the same directory.

2. **Open the terminal**
   - Go to `View` > `Terminal` in VS Code to open the terminal.

3. **Run the script**
   - In the terminal, type:
     ```bash
     python game.py
     ```
   - Replace `game.py` with the actual filename of your script if it's different.

4. **Play the game**
   - Use `W` and `S` keys to move the left paddle.
   - Use `Up` and `Down` arrow keys to move the right paddle.
   - The game ends when the ball passes behind a paddle, displaying a loss message.

## Controls
- **Player 1 (Left Paddle):** `W` (up), `S` (down)
- **Player 2 (Right Paddle):** `Up Arrow` (up), `Down Arrow` (down)

## Features
- Simple 2D Pong game using Pygame.
- Collision detection between ball and paddles.
- Ball speed and movement logic.
- Win/Loss conditions for each player.

## License
This project is for educational purposes and can be modified or expanded upon as needed.

