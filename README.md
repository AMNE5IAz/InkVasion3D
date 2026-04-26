# Inkvasion: 3D Paper Tank Warfare

Inkvasion is now a browser-playable 3D ink tank arena game. Pilot a blue sketch tank across notebook-paper battlefields, rotate the turret independently, and erase hostile red ink tanks before they smudge you out.

## Play

Open `index.html` in a modern browser. The game is static and can be hosted directly on Vercel, GitHub Pages, or any static host.

The first screen is now a menu:

- **Battles:** create a battle or quick join one, choose the mode, map, enemy count, and teammate count.
- **Garage:** choose your tank hull and turret before launching.
- Created battles appear in the Battles list; press **Join** to enter one. Match settings are locked once the battle starts.

## Controls

- Move: `W/A/S/D` or arrow keys
- Rotate turret: `Q/E` or `Z/X`
- Tap `Space`: fire an ink shot
- Hold `Space`: charge a full ink splash; when the bar fills, it launches a heavy splash attack
- Restart current page: `R`
- Next/previous page: `N` / `P`
- Open menu / pause setup: `Esc`

## Gameplay

- Third-person 3D arena camera inspired by arcade tank battlers.
- Four huge sketchbook arenas built for exploration and cover: Ink Wastes, Folded City, Blot Flag Basin, and Three Point Spillway.
- Maps now include walls, hills, ramps, raised paper structures, black ink rivers, bridges, erasers, pen holders, sharpeners, bases, and control zones.
- Battle creation supports Deathmatch, Team Deathmatch, Capture The Flag, and Control Points with locked match settings.
- Capture The Flag uses teams, flag capture targets, and a time limit.
- Control Points uses teams, rotating active points, score targets, and a time limit.
- Deathmatch has no teammates; everyone is hostile.
- Diverse tank hulls and turret choices appear visually in Garage and change in-game shape/stats.
- Enemy and ally AI patrols the large maps, avoids obstacles, recovers from wall contact, detects targets with line-of-sight, and moves toward mode objectives.
- Projectiles damage tanks and leave ink splatter marks on impact.
- Victory depends on the mode: erase enemies, soak the flag, or capture all control points.

## Implementation Notes

The current playable build is a static Three.js WebGL implementation so the game can run directly from GitHub Pages or a local static folder. The code keeps the planned Unity-style gameplay boundaries in JavaScript classes: `TankController`, `TankHealth`, `Projectile`, `EnemyTankAI`, `LevelDefinition`, and `GameManager`.

Unity can still be introduced later as a full engine migration, but this version delivers the planned 3D gameplay in the existing web repository without requiring a Unity build pipeline.
