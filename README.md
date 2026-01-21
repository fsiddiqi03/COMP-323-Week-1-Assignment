# Intro Arcade (Week 1 in-class build)

A simple first-week game to introduce Python + Pygame fundamentals.

## Learning goals
- Pygame setup: window, clock, main loop
- Events + input handling
- Game state: title → playing → game over
- Update/draw separation and delta time (`dt`)
- Simple collision using `pygame.Rect`
- Score + high score saved to `save.json`

## Run

```bash
python -m pip install pygame
python main.py
```

## Controls
- Arrow keys / WASD: move
- Enter: start / restart
- Esc: quit

## Save data
Writes `save.json` (high score only). Delete it to reset.

## Changes 
- Added new object called "Special Coin", when player get the "Speacial Coin" they get an invincible perk which lasts 5 seconds 
- Added new player state: self.player_state: str = "normal"  # normal | invincible
- Invincible is displayed in the top left when the user is that state, drawn via the def _draw_invincible(self) function 

# Scope Note 
- Added an invincible coin, when players get this coin they can not die to the enimies for 5 seconds. Simple addition that does not break the main loop and gives players a chance to get a higher score. 