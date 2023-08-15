# Emulator
## Setting it up
Setting up the emulator is easy! Everything should come ready to use out of the box. Simply copy the entire 'EmulatorComponents' folder from the Emulator repository and paste it into 'POINT-VR-Chapter-1\POINT-VR-Chapter-1\Assets\POINT' in your point project.
To use the emulator, open the 'PlayerBase' object within the scene menu and in the inspector window find the 'PlayerSpawner' script and set the player field to the 'PlayerEmulator' prefab. 
Now when you start the scene the emulator should spawn! If you have issues feel free to reach out to George Bayliss for help.

**Note:** When you push to github be sure to revert this last change, otherwise the Emulator will spawn when running the project in a headset.

## Controls
Movement:
 - WASD for motion in the player's xz plane 
 - 1 and Q for motion in the true y-direction
 - Arrow keys for player rotation
 - R resets vertical rotation

Laser:
 - Laser direction is controlled by the mouse
 - Mouse click will interact with UI and toggle grab when hovered over a grabbable
 - Scroll wheel to push and pull

 - P opens the pause menu

These controls are the ones which I have found to be most convenient, however feel free to change any of the bindings for your own ease of use.

## Adjustable Fields
The emulator comes with a few settings which you can edit to make the controls smoother for your experience.

- Within the 'Turn Controller Emulator' script of the 'PlayerEmulator' object, the 'TurnIncrement' and 'MotionIncrement' parameters control how quickly the Emulator turns and moves.
- In the 'Laser Controller' script of the 'RightHand' object, the 'TurnIncrement' parameter controls how sensitive the laser is to mouse movements.
- In the 'Hand Controller Emulator' script od the 'Hand' object, the 'ScrollSensitivity' parameter determines how sensitive pushing and pulling is with the scrollwheel.
- There are many additional parameters that can be changed though these are the most noticable ones.

## Known Issues
This emulator does not interface with the XR Controller so it has certain limitations. 

 - The emulator does not work with scene switching via the UI menu. 
	- Scene switching can be made to work with two adjustments: by commenting lines 36 and 74 in the 'SceneController' script and by editing the PlayerBase object (as done when setting up the emulator) for every relevant scene.
 - If switching scenes via the UI menu as noted above, the clocks will be non-functional in any scene that is switched to.

If you find any other issues with the emulator please reach out to George Bayliss or edit this README directly.

## General notes
The purpose of the emulator is foremost to be easy and comfortable to use. There are some unavoidable imperfections such as the perspective making it hard to see where the laser is, or that the controls (especially the mouse) can feel clunky at times, however for the most part it's should feel smooth and intuitive.
The 'EmulatorComponents' folder includes all the emulator-specific assets used for the emulator. Other assets will be in their usual place within the Chapter 1 repository.
All emulator-specific scripts are fully commented. 

Last updated 8/15/23
