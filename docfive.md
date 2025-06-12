### Developer Tasks
***

## Adding a new celestial object type
# Overview:
This guide details how to add a new type of celestial object (e.g., a comet) to Orbituary using Unreal Engine.

# Prerequisites:
- Access to the Orbituary Unreal Engine Project (Message developer to access)
- Familiarity with Unreal Engine’s Blueprint or C++ workflow
- 3D model and textures you created for the new object

# Steps:
1. Open the project.
> Launch Unreal Engine and open the Orbituary project.

2. Import the new asset.
> 1. In the Content Browser, right-click and select **Import to /Game/Objects.** 
> 2. Choose your 3D model and textures for the new celestial object.

3. Create a blueprint class.
> 1. Right-click in the Content Browser, select **Blueprint Class,** and choose **Actor**.
> 2. Name it BP_Comet (or relevant)

4. Add components.
> 1. Open your blueprint. 
> 2. Add your imported mesh as a Static Mesh Component. 
> 3. Attach any particle systems or VFX needed. 

5. Set up physics and interactions.
> In the Blueprint, enable physics simulation and set collision properties to match other destructible objects. 

6. Implement destruction logic.
> Add event logic for when the object is hit (e.g., by the player or projectiles). Trigger destruction effects and scoring. 

7. Place in level and test.
> 1. Drag the blueprint into a test level. 
> 2. Play the game to ensure the object behaves as expected.

> The new object should appear in-game, interact with the player, and trigger destruction and scoring as designed.

8. Commit changes.
> Save your work and commit/push changes to the project repository.

***
## Updating the Scoring System for New Objects
# Overview:
This guide explains how to update the scoring system to account for new celestial object types in Orbituary.

#Prerequisites:
- Access to the Orbituary Unreal Engine project.
- Knowledge of the current scoring system implementation

#Steps:
1. Locate Scoring Logic.
> In Unreal Engine, find the Blueprint class responsible for handling score updates. **BP_Gamemode**.

2. Add Scoring Rules.
> Add a new case or branch for the new object type (e.g., comet). Assign a score value for destroying this object.

3. Update Destruction Events.
> In the new object’s Blueprint or class, ensure destruction triggers the scoring event, passing the correct object type.

4. Test Scoring.
> In a test play, destroy the new object and verify that the correct score is awarded and displayed in the UI.

5. Document Changes.
> Update the internal documentation or comments to reflect the new scoring rule.

6. Commit changes.
> Save your work and commit/push changes to the project repository.
