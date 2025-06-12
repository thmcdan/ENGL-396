### Orbiturary Data Structure Reference

***
# Celestial Object Blueprint Structure

| Property	| Type |	Description |	Example Value |
| --------- | ---- | ------------ | ------------- |
| Name |	String |	Unique object identifier |	“BP_Asteroid” |
| Mesh |	Static Mesh |	3D model asset reference	| SM_AsteroidMesh |
| PhysicsEnabled |	Boolean |	Enables real-time physics interactions |	TRUE |
| Destructible |	Boolean |	Can be destroyed by player/projectiles |	TRUE |
| ScoreValue |	Integer |	Points awarded for destruction |	100 |
| VFX |	ParticleSystem |	Visual effect on destruction |	PS_AsteroidExplode |
| SFX |	SoundCue |	Sound effect on destruction |	SC_AsteroidBreak |

**Example: Adding a New Celestial Object (e.g., Comet)**
1. **Import Asset:** Add 3D model and textures to **GameObjects**.
2. **Create Blueprint:** Right-click -> Blueprint Class -> Actor -> Name: **BP_Comet**.
3. **Setup Components:** Assign mesh, add particle systems.
4. **Physics:** Enable simulation, set collisions.
5. **Destruction Logic:** Add event for hit, trigger VFX/SFX, update score.
6. **Test:** Place in level, verify behavior and scoring.
7. **Document:** Update internal docs/comments

***

# Scoring System Logic
- Object Types: Asteroid, Moon, Planet, Comet (customizable)
- Score Assignment: Each type has a `ScoreValue` property.
- Destruction Event: On object destruction, triggers event to add score.
- Combo Multiplier: Consecutive destruction increases multiplier.

**Example Blueprint Pseudocode**
```
blueprint<br>
Event OnDestroyed<br>
    AddScore(ScoreValue * ComboMultiplier)<br>
    PlayVFX()<br>
    PlaySFX()<br>
```

# Orbituary Glossary

|Term |	Definition|
|-----|-----------|
|Blueprint|	Unreal Engine’s visual scripting system for game logic and object behaviors.|
|Static Mesh|	A 3D object used for visual representation in-game.|
|VFX|	Visual Effects, such as explosions or comet trails, triggered during gameplay events.|
|SFX|	Sound Effects, audio cues for actions like destruction or upgrades.|
|Combo| Multiplier	A scoring mechanic that increases points for consecutive destruction actions.|
|Actor|	An object in Unreal Engine that can be placed in a level, such as the player or an asteroid.|
***
# Error Codes & Troubleshooting (Quick Reference Table)

|Error Code |	Description	Solution|
|-----------|---------------------|
|E001|	Game fails to launch	Check system requirements, run as admin|
|E002|	Unrecoverable error	Relaunch game. If issue persists, reinstall game |
|E003|	Graphics glitches	Update GPU drivers|

***
# Changelog

**Orbituary 0.05 (first revision)**
- Skybox has been updated to be less painful to look at, and is more seamless.
- Collision tube always acts as collision, doesn't let player out with no way back in.
- Cat no longer jitters when walking on home planet
- End game menu brought back to make it clear when the level ends
- Cursor no longer invisible in main menu
- Shooting abilities no longer affect player (except the explosion of the standard shot, which may be kept or removed)
- tweaked the speed and control of different abilities and mechanics
- aesthetic fix (that greatly improved the look and feel.)
- Added a few minor additional fixes and features

**Orbituary Build 0.06 (Latest Build)**<br>
*Added:*
- Created variables for shot recharging/cooldown
- Scoreboard
- Explosion particles when celestials get hit
- Camera sensitivity and Master volume settings

*Improved:*
- Adjusted shooting strength, size, impact
- Made the skybox less blindingly disorienting
- Cat orients correctly when landing on planet (but it's instantaneous; no transition)
- Comet tail and shooting particles
- Adjusted lighting
- Improved menus and added updated controls

*Fixed:*
- Player clipping through collision tube
- Shots colliding with player
- Cursor vanishing in menus
- Removed cat from Main Menu
- Cat jittering when walking on planet
- High score system now actually saves high scores
- Helix shot now rotates correctly
- Light-speed energy bar no longer stutters when released before depleting to 0 



###### For further details on gameplay mechanics, see the Gameplay Documentation. For installation help, see the Task Documentation. For developer implementation, refer to the Technical Overview.



