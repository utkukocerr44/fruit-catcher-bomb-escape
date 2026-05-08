# Fruit Catcher: Bomb Escape

Fruit Catcher: Bomb Escape is a browser-based arcade game developed with HTML5 Canvas and JavaScript for the Computer Graphics final project. The player controls a character inside the canvas, collects apples to increase the score, avoids falling bombs, and tries to survive as the difficulty increases.

The game was designed as a simple but complete arcade experience with a clear start, play, pause, game over, and restart loop. It includes scoring, increasing difficulty, multiple power-ups, hazards, visual feedback, and a persistent high-score system.

## Play the Game

GitHub Pages link:

https://utkukocerr44.github.io/fruit-catcher-bomb-escape/

## Controls

- **Space**: Start the game
- **Arrow Keys**: Move the player
- **P**: Pause / resume the game
- **R**: Restart after game over

When the player resumes from pause, the game shows a short 3-2-1 countdown before continuing.

## Objective

The objective is to collect as many apples as possible while avoiding bombs. The player starts with three lives. If the player collides with a bomb, one life is lost. The game ends when all lives are lost.

The score increases by collecting apples and special items:

- Normal apple: **+10 points**
- Golden apple: **+50 points**

The game stores the highest score locally in the browser using `localStorage`.

## Game Features

### Increasing Difficulty

The game becomes more difficult as the score increases. Every 50 points, the level increases and an additional bomb is added. This creates a longer gameplay loop and keeps the challenge increasing over time.

### Power-Ups

The game includes several temporary power-ups:

- **Candy / Slow Motion**: slows bombs for a short time.
- **Magnet**: pulls apples and golden apples toward the player.
- **Golden Heart**: restores one life if the player has lost health. If the player already has full health, it gives a temporary bonus heart.
- **Golden Apple**: a rare collectible that gives a higher score bonus.

Power-ups disappear if they are not collected in time. Some effects also blink near the end of their duration to show the player that they are about to expire.

### Hazards

In addition to falling bombs, the game includes a rare skull hazard. If the player touches the skull, it triggers **Bomb Storm**, temporarily adding extra bombs and increasing the danger. After the storm ends, the extra bombs leave the screen naturally instead of disappearing immediately.

### Visual Feedback

The game uses several visual effects to make actions clearer:

- Screen shake when the player is hit by a bomb
- Particle effects when collecting items or taking damage
- A colored Bomb Storm overlay
- Magnet aura around the player
- Blinking effects for temporary items
- Floating score and damage text
- Level-up animation

## Computer Graphics Concepts Used

This project demonstrates several computer graphics concepts:

- **Canvas rendering**: all game objects, UI text, overlays, and effects are drawn on the HTML5 Canvas.
- **Animation loop**: `requestAnimationFrame` updates the game state and redraws the scene continuously.
- **Collision detection**: the game checks collisions between the player, apples, bombs, hazards, and power-ups.
- **Transformations**: `translate`, `scale`, and `rotate` are used for screen shake, countdown animation, golden apple animation, and level-up effects.
- **Particle system**: particles use position, velocity, gravity, alpha fading, and lifetime values.
- **Game state management**: different states such as start, play, pause, countdown, game over, and restart are handled in JavaScript.

## Project Structure

```text
fruit-catcher-bomb-escape/
├── index.html
└── README.md
```

The full game is contained in `index.html`, including the HTML structure, CSS styling, canvas setup, and JavaScript game logic.

## Author

**Yılmaz Utku Koçer**  
Student ID: **220303040**

