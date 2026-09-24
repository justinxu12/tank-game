# Tank Game

A 2D tank battle game written in C using SDL2. The game supports both single-player battles against an AI-controlled opponent and local two-player gameplay, with multiple tank classes, projectile mechanics, obstacles, health systems, sound effects, and interactive menus.

The project is built on a custom game and physics library that handles rendering, rigid bodies, collisions, forces, scenes, input, and game state management.

## Features

### Game Modes
- Single-player mode against an AI-controlled tank
- Local two-player battles
- Tank selection menu
- Score tracking and game-over screens
- Health bar system

### Tank Classes

Players can choose between four tank types with different movement, health, weapon, and reload characteristics:

- **Default** — balanced movement and combat
- **Gravity** — uses gravity-based projectile mechanics
- **Sniper** — slower tank with high-velocity, high-damage shots
- **Gatling** — rapid-fire tank with a faster reload rate

### AI Opponent

Single-player mode includes an AI-controlled opponent that:

- Aims toward the player's position
- Fires when aligned with the player
- Switches between multiple movement behaviors
- Adjusts movement over time during combat

### Physics & Collision System

The game uses a custom C physics library for:

- Rigid-body representation
- Polygon-based collision detection
- Collision response
- Force and impulse handling
- Object velocity and movement
- Scene and body management

### Graphics, Audio & UI

SDL2 is used to provide:

- Real-time 2D rendering
- Keyboard and mouse input
- Tank and projectile sprites
- Menu and game-over interfaces
- Text rendering with SDL_ttf
- Music and sound effects with SDL_mixer

## Architecture

```text
tank-game/
├── assets/          # Tank sprites, audio, and fonts
├── demo/
│   └── game.c       # Tank game logic, UI, AI, and gameplay
├── include/         # Public interfaces for the game/physics library
├── library/         # Physics, rendering, collision, and data structures
├── tests/           # Unit tests for core library components
└── README.md
```

### Game Layer

`demo/game.c` contains the primary game logic, including tank creation, projectile handling, AI behavior, menus, health systems, scoring, and game-state transitions.

### Engine Layer

The reusable library provides abstractions for bodies, scenes, vectors, polygons, collisions, forces, rendering, text, and supporting data structures. This separates lower-level engine functionality from the tank game's gameplay logic.

## Testing

The repository includes unit tests for core engine components, including:

- Bodies and scenes
- Collision detection
- Forces
- Vectors and polygons
- Lists and maps
- Color utilities

## Tech Stack

- C
- SDL2
- SDL_mixer
- SDL_ttf

## Author

Justin Xu
