# Inkvasion: 3D Paper Tank Warfare

Inkvasion is now a browser-playable 3D ink tank arena game. Pilot a blue sketch tank across notebook-paper battlefields, rotate the turret independently, and erase hostile red ink tanks before they smudge you out.

## Play

Open `index.html` in a modern browser. The game is static and can be hosted directly on Vercel, GitHub Pages, or any static host.

## Controls

- Move: `W/A/S/D` or arrow keys
- Rotate turret: `Q/E` or `Z/X`
- Tap `Space`: fire an ink shot
- Hold `Space`: charge a full ink splash; when the bar fills, it launches a heavy splash attack
- Restart current page: `R`
- Next/previous page: `N` / `P`
- Switch mode label: `M`

## Gameplay

- Third-person 3D arena camera inspired by arcade tank battlers.
- Four larger sketchbook arenas built for exploration and cover: Ink Wastes, Folded City, Blot Flag Basin, and Three Point Spillway.
- Game mode rules inspired by arena tank games: Deathmatch, Team Deathmatch, Capture The Flag, and Control Points.
- Diverse tank archetypes: Striker, Scout, Heavy, and Rail-style enemies with different health, speed, barrels, and damage.
- Enemy tanks patrol, detect the player with line-of-sight, chase, aim, and fire.
- Projectiles damage tanks and leave ink splatter marks on impact.
- Victory depends on the mode: erase enemies, soak the flag, or capture all control points.

## Implementation Notes

The current playable build is a static Three.js WebGL implementation so the game can run directly from GitHub Pages or a local static folder. The code keeps the planned Unity-style gameplay boundaries in JavaScript classes: `TankController`, `TankHealth`, `Projectile`, `EnemyTankAI`, `LevelDefinition`, and `GameManager`.

Unity can still be introduced later as a full engine migration, but this version delivers the planned 3D gameplay in the existing web repository without requiring a Unity build pipeline.
