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

# Week 1 Changes 
- Added new object called "Special Coin", when player get the "Speacial Coin" they get an invincible perk which lasts 5 seconds 
- Added new player state: self.player_state: str = "normal"  # normal | invincible
- Invincible is displayed in the top left when the user is that state, drawn via the def _draw_invincible(self) function 

### Week 1 Scope Note 
- Added an invincible coin, when players get this coin they can not die to the enimies for 5 seconds. Simple addition that does not break the main loop and gives players a chance to get a higher score. 



# Week 2 Changes
### New Wave
- Spawns 3 additional enemies when the player's score exceeds 10, bringing the total from 3 to 6
- Players must decide whether to play aggressively to maintain high scores or play cautiously as the playfield becomes more crowded
- Player learns higher scores come with increased risk, teaching resource management and spatial awareness
### New Hazard
- If the player touches any edge of the playfield, their score resets to 0
- Players must balance speed to collect coins and dodge enemies 
- This teaches players boundaries are not safe zones, the entire playfield requires attention, showing careless movement has consequences
