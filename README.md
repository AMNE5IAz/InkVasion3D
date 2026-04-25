# Inkvasion: 3D Paper Tank Warfare

Inkvasion is now a browser-playable 3D ink tank arena game. Pilot a blue sketch tank across notebook-paper battlefields, rotate the turret independently, and erase hostile red ink tanks before they smudge you out.

## Play

Open `Game/index.html` in a modern browser, or use the root `Inkvasion.html` redirect.

## Controls

- Move: `W/A/S/D` or arrow keys
- Rotate turret: `Q/E` or `Z/X`
- Fire: `Space`
- Restart current page: `R`
- Next/previous page: `N` / `P`

## Gameplay

- Third-person 3D arena camera inspired by arcade tank battlers.
- Five sketchbook arenas: Open Fields, Urban Ruins, Mountain Pass, Corridor Lanes, and Blank Training Page.
- Enemy tanks patrol, detect the player with line-of-sight, chase, aim, and fire.
- Projectiles damage tanks and leave ink splatter marks on impact.
- Victory triggers when every hostile ink tank on the page is erased.

## Implementation Notes

The current playable build is a static Three.js WebGL implementation so the game can run directly from GitHub Pages or a local static folder. The code keeps the planned Unity-style gameplay boundaries in JavaScript classes: `TankController`, `TankHealth`, `Projectile`, `EnemyTankAI`, `LevelDefinition`, and `GameManager`.

Unity can still be introduced later as a full engine migration, but this version delivers the planned 3D gameplay in the existing web repository without requiring a Unity build pipeline.
