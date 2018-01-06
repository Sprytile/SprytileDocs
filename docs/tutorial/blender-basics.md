# Blender Basics

If you're new to Blender, this section of the tutorial will teach the Blender basics to confidently use Sprytile.

Blender is an [open source 3D software package](https://www.blender.org/) that is free to use. It is incredibly versatile and can handle many 3D tasks. For Sprytile, we'll be using it for its 3D modeling capabilities.

Start by [getting the latest recommended version](https://www.blender.org/download/) of Blender from the download page and installing it. Don't download a Release Candidate.

Run Blender after installation and you will see the following screen. The splash screen artwork may be different depending on the version you installed.

## Window Areas

Click outside the splash box and you should see this. This is the default layout of the Blender window. The labeled parts are what we'll be using while working with Sprytile.

The window areas can be resized to better fit your needs by moving the mouse between areas and dragging when indicated. 

### 3D View

The window used to interact with the 3D scene we're working with. This where we'll be spending most of our time working in Blender.

### Tool Shelf

Technically part of the 3D view, the tool shelf is a convenient place for Blender's various tools. It is also where we'll interact with Sprytile's tools when Sprytile is installed.

If the tool shelf disappears while you're working with Blender, press the `T` key while your mouse is over the 3D view to show it again.

### Properties View

The properties panel is used for setting the data for Blender's various components. We will not use this with Sprytile but it is useful to know where it is.

### Outliner

This lists the objects in the 3D scene. Useful when there are multiple objects in the scene.

## Camera Navigation

Now we'll learn how to move around in the 3D view. This is important to learn as this is how we'll move around while editing the scene.

!!! note "No Middle Mouse Button?"

	If you do not have a middle mouse button, follow the [instructions in this video](https://www.youtube.com/watch?v=qdqEYfSb6t8) to enable three button mouse emulation, and hold down the `Alt` key in the following instructions.

When you want to move around in 3D view, the mouse cursor must start from inside the 3D view before holding down the middle mouse button. Releasing the middle mouse button will stop moving the 3D view.

### Rotation/Panning

Hold down the `middle mouse` button and move the mouse around. This rotates the view around a focus point. The focus point will be discussed later in the tutorial.

### Horizontal/Vertical Movement

1. Hold down the `Shift` key
2. Hold down the `middle mouse` button
3. Move the mouse around

This moves the camera along horizontal and vertical axis that the camera is facing.

### Forward/Backward Movement

1. Hold down the `Ctrl` key
2. Hold down the `middle mouse` button
3. Move the mouse up and down

When the mouse is moved upwards, the camera moves forward towards the direction it is facing, and reverses when the mouse is moved down.

### Orthogonal Views

It's sometimes useful to view the scene from the top, side, or front view. These are called orthogonal views and can easily be accessed from Blender by using the number pad, the grid of numbers on the right side of the keyboard.

* `Numpad 1`: Front view
* `Numpad 3`: Right view
* `Numpad 7`: Top view

Holding `Ctrl` and pressing the above keys will give a view from the opposite side.

If your keyboard does not have a number pad, or are looking for a supported alternative workflow check out the officially supported [Pie Menu Addon](https://www.youtube.com/watch?v=ioYWPmnhNtY).

### Orthographic Toggle

Pressing `Numpad 5` will toggle between orthographic and perspective projection.

Orthographic projection will draw the 3D view without perspective and foreshortening, which may be useful for lining up objects in the scene or getting a clearer sense of the use of space in the scene.

---

Practice moving the 3D view around until you're comfortable with it. Being able to navigate in 3D easily is important when working in 3D.

## Working with Objects

Now we'll learn how to edit objects in Blender.

### Selection

Blender's starting scene contains a cube mesh, a camera, and a lamp. Each of these are different kinds of objects inside Blender. 

By default, the cube mesh is selected. You can tell this by the outline around the cube, or the by the circle selected indicator in the scene outliner.

Let's try selecting the camera by `right clicking` on the triangular object to the left of the scene. The camera is now highlighted in the 3D view and the scene outliner.

### Transformation


#### 3D Manipulator

#### Shortcut Keys

## Context Modes

### Object Mode

### Edit Mode

## 3D Cursor

## Useful Shortcuts

* `Tab` - Toggle context mode
* `Numpad Del` - Focus 3D view on selection
* `Shift Space` - Focus window on view