# PAC-ADEMIC

Pac-Man played in our university building: three buildings (A, B, C), five floors each.
It runs entirely in the browser (one `index.html`, no server, no backend), so it can be hosted on GitHub Pages.

## The maze
- Each building floor is a zone (A1 … C5), and each zone is a small Pac-Man board.
- **Floors 1–3 (the hub):** corridors link the buildings A↔B↔C. Floor 1 also has a direct A↔C side tunnel. This link isn't confirmed yet, so you can turn it off under *Options*.
- **Stairs:** every building has stairs between adjacent floors. Floors 1↔2↔3 and 4↔5 have two stairwells each. Floor 3↔4 has just **one**, which is the chokepoint.
- **Floors 4–5 (branches):** these floors have no corridors, so you can only leave them by going back down the stairs. Most power pellets are up here, so going up is a risk with a reward.
- Ghosts pick their moves from shortest paths on the tile graph (a BFS over corridors and stairs only).

## Ghosts
| Ghost | Behaviour |
|---|---|
| Blinky | Chases you along the shortest path, and speeds up when few dots are left |
| Pinky | Aims 4 tiles ahead of you |
| Inky, the Gatekeeper | Guards the floor-3 stairwell when you're on floors 4–5. Otherwise he blocks the corridor or staircase nearest to you |
| Clyde | Chases you from a distance and backs off when he's close |

Ghosts move slower on the stairs. Press **G** to see each ghost's planned path.

## Controls
Use the arrows or WASD to move. On a phone, swipe or use the D-pad. **P** pauses the game and **M** toggles sound.

## Run locally
Open `index.html` in a browser.
