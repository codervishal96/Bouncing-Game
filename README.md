# Bouncing Ball Game

A simple arcade game built with Python and Pygame. Move the platform left and right to keep the ball in play, score points with every bounce, and survive as many levels as you can.

## Features

- Smooth platform movement with the arrow keys
- Ball that bounces off the walls, the ceiling, and your platform
- Score, level, and lives shown in colored boxes at the top of the screen
- Level system: you advance every 10 points
- Platform changes to a random color each time you level up
- Start screen and Game Over screen with restart support
- 5 lives per game

## Requirements

- Python 3.8 or newer
- [Pygame](https://www.pygame.org/)

## Installation

1. Clone or download this project.
2. Install Pygame:

   ```bash
   pip install pygame
   ```

## How to Run

```bash
python main.py
```

## How to Play

| Action | Control |
| --- | --- |
| Start the game / restart after Game Over | Press any key |
| Move platform left | Left Arrow |
| Move platform right | Right Arrow |
| Quit | Close the window |

**Rules**

1. The ball bounces off the left wall, right wall, and top of the screen.
2. Catch the ball with the platform to bounce it back up and earn **1 point**.
3. If the ball falls past the bottom of the screen, you lose **1 life**.
4. Every **10 points** takes you to the next level. The ball resets to the center with a new random speed, and the platform changes color.
5. When all 5 lives are gone, the Game Over screen shows your final score. Press any key to play again.

## Project Structure

```
.
├── main.py      # Complete game code
└── README.md    # Project documentation
```

## Configuration

You can tweak the game by editing the constants and variables near the top of `main.py`:

| Setting | Default | Description |
| --- | --- | --- |
| `WIDTH`, `HEIGHT` | 800, 600 | Window size |
| `BALL_RADIUS` | 20 | Size of the ball |
| `PLATFORM_WIDTH`, `PLATFORM_HEIGHT` | 100, 20 | Size of the platform |
| `FPS` | 60 | Frame rate |
| `platform_speed` | 5 | How fast the platform moves |
| `lives` | 5 | Starting lives (set in `reset_game()`) |

## Code Overview

- `reset_game()` – resets the ball, platform, score, lives, and level
- `start_screen()` / `game_over_screen()` / `victory_screen()` – full-screen messages that wait for a key press
- `show_text_on_screen()` – helper that draws centered text
- `wait_for_key()` – pauses until the player presses a key
- `change_platform_color()` – returns a random RGB color for the platform
- Main loop – handles input, ball and platform movement, collisions, scoring, leveling, drawing, and frame rate

## Ideas for Improvement

- Use `victory_screen()` when the player reaches a final level
- Add sound effects and background music
- Make the ball speed up as the level increases
- Save and display a high score
- Change the bounce angle based on where the ball hits the platform
- Add a pause key

## License

This project is free to use and modify for learning and personal projects.
