# Asteroids

A simple **Asteroids-style arcade game** built with **Python** and **Pygame**.  
Fly your ship, dodge incoming asteroids, and shoot them apart before they hit you.

## Features

- Classic top-down Asteroids gameplay
- Player movement and rotation
- Shooting with cooldown
- Asteroids spawn from the edges of the screen
- Larger asteroids split into smaller ones when hit
- Game state and event logging in JSONL format

## Controls

- **W / S** — Move forward / backward
- **A / D** — Rotate left / right
- **Space** — Shoot

## Requirements

- Python **3.13+**
- `pygame==2.6.1`

## Installation

```bash
git clone https://github.com/anurag342-dot/asteroids.git
cd asteroids
```

If you are using `uv`:

```bash
uv sync
```

Or install dependencies manually:

```bash
pip install pygame==2.6.1
```

## Run the Game

```bash
python main.py
```

## How It Works

The game opens a `1280 x 720` window and runs the player, asteroids, and shots using Pygame sprite groups. The player moves using keyboard input, asteroids spawn automatically from random screen edges, and collisions are checked every frame. If the player collides with an asteroid, the game ends. When a shot hits an asteroid, the asteroid splits into smaller pieces if possible.

## Project Structure

```text
asteroids/
│
├── main.py              # Main game loop and initialization
├── player.py            # Player ship movement, rotation, shooting
├── asteroid.py          # Asteroid creation, movement, splitting logic
├── asteroidfield.py     # Asteroid spawning system
├── shot.py              # Bullet/shot behavior
├── circleshape.py       # Base class for circular game objects
├── constants.py         # Game settings and constants
├── logger.py            # Game state and event logging
│
├── game_state.jsonl     # Generated game state logs
├── game_events.jsonl    # Generated event logs
│
├── pyproject.toml       # Project configuration and dependencies 
├── .python-version      # Python version configuration
├── .gitignore           # Git ignored files
└── README.md            # Project documentation
```

## Logs

This project includes lightweight logging for debugging and analysis:

- `game_state.jsonl` stores periodic snapshots of the game state
- `game_events.jsonl` stores important events like asteroid hits, splits, and player collisions

## Notes

This is a clean, minimal arcade project focused on gameplay, movement, collisions, and spawning logic.  
It is a great base for adding a score system, lives, sound effects, menus, or a restart screen.

---

Made with Python and Pygame.

