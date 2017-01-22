# Quick Start Tutorial #

This is a short tutorial on how to install and use Sprytile. We'll be using the following tile set image for this tutorial, but feel free to use your own tileset to follow along.

![Tile Set](img/tileset.png)

## Installation ##

Download the zip file from the [Sprytile page](https://chemikhazi.itch.io/sprytile).

In Blender, open User Preferences by going to `File > User Preferences`. Go to the Add-ons tab and press  `Install from File` at the bottom of the preference window and navigate to the downloaded zip file. After installation, search for Sprytile under Community addons and enable it.

![Install Addon](img/install-addon.png)
![Enable Addon](img/enable-addon.png)

!!! note "Future Uses"

    Press the `Save User Settings` button if you want to continue using Sprytile in future Blender sessions without going to User Preferences

With Sprytile installed, let's start a new Blender file by going to `File > New`. Make sure the tool shelf panel to the left of the 3D view is open. If it is not, press `T` and find the Sprytile tab. If the Sprytile tab is missing, check the installation steps again.

## Material Setup ##

Before using the Sprytile tools, the tile set has to be loaded into the material. With a mesh object selected, go to the Materials tab in the Properties View, then press `Set Material to Shadeless` in the Sprytile panel.

![Material Setup](img/setup-material.jpg)

Next, go to the Textures tab in the Properties view and load your tile set image into the material. After loading the image, go back to the Sprytile tab and press `Setup Pixel Texture`.

![Texture Setup](img/setup-texture.png)

## Sprytile Tools ##

The majority of Sprytile tools are accessed under `Edit Mode`. With a mesh object selected, enter edit mode and open the tool shelf to the Sprytile tab. Press `T` to open the tool shelf if it is hidden from the left of the 3D view. Expand the tool shelf if it is too cramped.

![Sprytile Edit Tools](img/edit-tool-shelf.png)

!!! tip "Pixel Density"

    If you're not using the provided tile set, you might want to change the world pixel density setting. This sets how many pixels fit inside one Blender unit. The provided tile set is based around 32x32 pixel tiles.

## Build Tool ##

The build tool creates mesh faces that are UV mapped to the selected tiles. Open Sprytile's tile map mode by pressing the `Build` button. You will notice the tile selection UI popup on the lower right corner of the 3D view, indicating that tile map mode is active.

Exit tile map mode by pressing the `Build` button again or by pressing the `Esc` key. Pressing `Ctrl + Shift + Space` on the keyboard will activate tile map mode again.

![Tile map mode](img/tile-map-mode.png)

!!! note "Tile Selection UI"

    The tile selection UI lets you pick the tile you will be painting with. Zoom the UI by hovering over it and scrolling your mouse wheel up or down.

### Tile Building Workflow ###

Now to get familiar with Sprytile's workflow by building something! First, delete the existing vertices of the selected mesh so we have a blank slate.

The workflow of Sprytile revolves around Blender's 3D cursor and the direction the 3D view is facing.

The 3D cursor is the center of the tile grid when you're painting, and the global axis that the view is facing is the surface you will be painting on.

As an example, reorient the 3D view so that it is facing the floor of the file, and then set the 3D cursor to the center by pressing `Shift + S` and selecting `Cursor to Center`.

![Paint Prepare](img/paint-prepare.png)

In the tile selection UI, choose the grass tile and paint around the 3D cursor. Notice how the tile grid is centered on the 3D cursor and the painting surface is oriented to the ground.

![Paint Z-axis](img/paint-1.png)

Now reorient the 3D view so it is facing one of the side facing global axis. Pick a wall tile and paint with the tile. Notice how the tiles are being created on a grid centered on the 3D cursor but now in a perpendicular direction.

![Paint Y-axis](img/paint-2.png)

!!! info "Axis Indicator"

    While tile map mode is activated, the axis indicator in the Sprytile Painter panel will update to show you which axis the tiles will be painted on.

    ![Axis Indicator](img/axis-indicator.png)

Since the 3D cursor is an important part of the Sprytile workflow, you can quickly reposition the cursor to the vertex nearest the mouse cursor by holding down the `S` key while in tile map mode. To make navigation easier as well, pressing the `W` key will center the 3D view around the cursor.

![Cursor Snap](img/cursor-snap.gif)

Try reorienting the 3D view to face the last axis you have yet to paint on, then moving the 3D cursor by holding down the `S` key and moving your mouse. Paint on that axis. Note that the center has moved to where you have positioned the cursor.

![Paint X-Axis](img/paint-3.png)

!!! bug "Beta software!"

    Sprytile is still in beta. If Sprytile stops responding during this tutorial, use the reset function under the utilities dropdown.

    ![Reset](img/reset-sprytile.png)

### Tile Grids ###

Now that you know how to use Sprytile, let's focus on tile grids. Tile maps may be made up of tiles in different scales. To account for this, Sprytile allows you to paint tiles in different sizes. This part of the Sprytile panel allows you to create and organize the grid settings used in the tile map.

Press the `+` button at the panel and select the newly created entry. The settings for this new tile grid can be changed in the boxes below. For this tile grid, lets change it to a 16 x 16 tile size.

![Tile Grid Panel](img/tile-grid-panel.png)
![Tile Grid Editing](img/tile-grid-edit.png)

You can see that the tile selection UI updates to show the currently selected tile grid as well. You can change the tile grid selection by using the panel, or holding `Ctrl` with your mouse over the tile selection UI and scrolling your mousewheel up or down.

![Tile Selection Update](img/tile-selection-update.png)

### Tile Flip/Rotation ###

Looking closely at the last wall we created, we can see that the texture gets very repetitive. By using the smaller tile grid we created, we can break up the pattern created by the larger tile size.

![Wall Small Tiles](img/wall-small-tiles.png)

But even with the smaller tiles, the repetition is still visible. With tile map editors, you can further break up the patterns by rotating and flipping tiles. To do that, we use this part of the Sprytile panel. For convenience, the keyboard shortcuts for rotating tiles left and right are the `1` and `2` keys.

![Flip/Rotate Panel](img/flip-rotate.png)

## Pixel Grid Translate ##

## Paint Tool ##
