# Godot-Virtual-Joystick
A simple virtual joystick for touchscreens, for both 2D and 3D games, with useful options.

<p align="center"> 
	<img src="https://raw.githubusercontent.com/MarcoFazioRandom/Godot-Virtual-Joystick/master/preview_icon.png" width="400">
	<img src="https://raw.githubusercontent.com/MarcoFazioRandom/Godot-Virtual-Joystick/master/preview_1.png" width="400">
</p>

Made with Godot Engine: https://godotengine.org

### OPTIONS:  

<img src="https://raw.githubusercontent.com/MarcoFazioRandom/Godot-Virtual-Joystick/master/preview_2.png" width="300">

- UI mode: 
	- Static: The joystick doesn't move. 
	- Moving: Every time the joystick area is pressed, the joystick position is set on the touched position. 
	- Following: If the finger moves outside the joystick background, the joystick follows it.  

- Vector mode: 
	- Normalized: return a normalized vector. 
	- Real: return a vector with a lenght beetween 0 and 1; useful for implementing different velocity or acceleration.  

- Directions: The number of directions, e.g. a D-pad is joystick with 4 directions, keep 0 for a free joystick.  
- Simmetry: It changes the angle of simmetry of the directions.  

- Dead zone: When the joystick value is less than the deadzone, the output is zero.  

- Clamp zone: The max distance the button can reach from the center.  

### HELP:  
- The Control parent of the joystick is the area in which the joystick can move in MOVING or FOLLOWING mode.  
- For moving the joystick inside is area, select it, right click and turn on "Editable Children" and simply move the 'Background' node.  - With "Editable Children" turned on you can also edit the joystick textures and colors.  
- An example scene is provided in the "Test" folder.  
- To be able to use the joystick with the mouse, you have to go to Project settings -> Input Devices -> Pointing, and turn on the option "emulate touch from mouse".  

### HOW TO USE:  
In your Player scene, add a CanvasLayer node as a child of it and name it "UI", it'll contain all the UI elements of the player, then add the Joystick scene as a child of the UI node and move it where you prefer (remember to turn on "Editable Children"). 