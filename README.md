# Animator Editor
This is a program can display an animation based on provided formatted text input.
Certain view options provide tools to edit the animation, similar to a simplified video editor.

# How to run
Open run configuration in IntelliJ by clicking Edit Configurations under the run tab.
Make a new application, select the class named Excellence as the main class.

Program arguments are as follows:

Required arguments:
-view <one of: text, svg, visual, edit, super>
-in inputs//<any *.txt file from the inputs folder>

Optional arguments:
-out <file path> (default output is to the console)
                 (If specified, this should be a *.txt or *.svg file)

-speed <integer> (default is 1 tick per second)

# What do the views look like?
# Text
-Returns formatted text representing the animation

# SVG
-Returns SVG formatted text

# Visual
-Displays the animation once

# Edit
1) Add/Delete shapes to the animation
2) Add/Edit/Delete keyframes of the animation
-A keyframe describes the attributes of a shape at a point in time in the animation
-A keyframe will contain information about a shape such as the position (xy-coordinates),
 width, height, color
3) Speed Scrubbing
-Adjust the speed of the animation
4) Load & Export
-Load a formatted text file to animate, or export the current animation as a *.svg or *.txt file
5) Enable/Disable Looping
-If looping is enabled, the animation will restart after it finishes

# Super
Includes all functionality in edit view as well as the following

1) Scrubbing
-The ability for a user to scrub by dragging a slider (or scrollbar) on the UI.

2) Rotation
-The ability to add a rotate animation in the input file, and changes to the file reader to
support such files.

3) Layers
-The ability to add, delete, or rearrange layers in the animation. 
A layer determines which shape is displayed if two shapes overlap. For example, if a
rectangle is on layer 0, and an oval is on layer 1, if the oval crosses paths with the rectangle 
in the animation, the oval will be displayed on top of the rectangle.
