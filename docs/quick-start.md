# Quick Start Tutorial

This is a short tutorial on how to use Sprytile **v0.5.2**, with Blender **2.9**. This also applies to Blender version 2.8.

We'll be using the following tile set image for this tutorial, but feel free to use your own tileset to follow along.

!!! note "tileset.png"
    <div style="align: center; width: 100%;">
    [![tileset.png](img/tileset.png)<br/>*Click to download*](img/tileset.png)
    </div>

## Installation

Download the zip file from the [itch.io page](https://chemikhazi.itch.io/sprytile). Sprytile can be downloaded for free, but donations are very much appreciated.

=== "1. Install Addon"

    In Blender, open User Preferences by going to `Edit > Preferences`. Go to the Add-ons tab and press the  `Install` button and navigate to the downloaded zip file.


    ![Install Addon](img/install-addon.png)

=== "2. Enable Addon"

    After installation, make sure you enable the addon by checking the box on the top left.

    ![Enable Addon](img/enable-addon.png)
    
    !!! note "Addon Preferences"

        There are preferences in the addon tab that you may want to change, according to your own workflow. You can always come back to these preferences when you figure out what works for you.

## Starting Sprytile

With Sprytile installed and setup, let's start a new Blender file by going to `File > New > General`.

In Blender 2.9, Sprytile shows up in the `Toolbar` to the **left** of the viewport, and in the `Sidebar` to the **right**.

If you don't see the toolbar on the left press the `T` key to show the tools, and if there are no panels on the right press the `N` key. You can also toggle them through the `View` menu.

![Toolbar and Sidebar](img/toolbar-sidebar.png)

If the Sprytile properties panel is not available in the right sidebar, make sure Sprytile is enabled in Blender's add-ons preferences.

## Sprytile Setup

Before using Sprytile tools, there are a couple of things to setup.

=== "Loading Tilesets"

    Sprytile needs to know the textures it is working with. Go to the Sprytile panel in the right sidebar and press `Load Tileset`. Choose the tileset texture and the material and texture are automatically setup. If you are using more than one tileset, use the `Add Tileset` button to make additional materials.

    ![Load Tileset](img/load-tileset.png)

=== "Viewport Setup"

    The default Blender viewport settings can make your textures look duller than intended. If you won't do any advanced rendering in your scene, you may want to use `Setup Pixel Viewport` in the Sprytile Utilities dropdown. There is an option in the Sprytile addon preferences to always use this setting.

    ![Viewport Setup](img/viewport-setup.png)

## Sprytile Tools

The majority of Sprytile's tools are accessed under `Edit Mode`. Select the default Blender cube, and enter edit mode by pressing the `Tab` key.

![Sprytile Edit Tools](img/sprytile-edit-tools.png)

## Build Tool ##

The build tool creates faces that are UV mapped to the selected tiles. Open Sprytile's tile map mode by pressing the `Sprytile Build` tool. The tile palette will appear on the lower left corner of the viewport, indicating that Sprytile is active.

![Sprytile Build Tool](img/tool-build.png)

If the palette is hidden by the toolbar, ==move the tile palette== by putting your mouse in the tile palette and holding the **shift key**. The scroll wheel ==zooms the palette in and out==.

![Arranging the Tile Palette](img/tool-palette-arrange.gif)

Exit the build tool by going into any of Blender's other tools. Pressing the `W` key will take you to Blender's select tool.

First, delete the existing vertices of the cube so we have a blank slate. Do this by pressing `A` to select all, and then pressing `X` and selecting `Vertices`.

Sprytile's workflow revolves around Blender's 3D cursor and the direction the 3D view is facing.

The 3D cursor is the center of the tile grid when you're painting, and the global axis that the view is facing is the surface you will be painting on.

Let's start by reseting the 3D cursor to the center of the scene by pressing `Shift + S` and selecting `Cursor to World Origin`.

![Paint Prepare](img/paint-prepare.png)

While in the build tool, try rotating the 3D view camera around. Hold down the middle mouse button while the mouse cursor is in the 3D view and move the mouse.

![Camera Pan](img/camera-pan.gif)

Notice that a grid appears around the blender 3D cursor. This is called the ==work plane== and indicates the plane that you'll be placing tiles onto.

By default, the work plane appears when the view camera is panned. If it does not, [check the settings](/advanced-features/#work-plane-cursor).

Tilt the camera downwards so that the work plane is aligned to the ground.

In the tile palette, choose the grass tile and paint around the 3D cursor. The grid is centered around the 3D cursor and the painted tiles appear on the ground, as shown by the work plane.

![Paint Z-axis](img/paint-1.gif)

Now pan the camera up so the work plane is vertical. Pick a wall tile and paint with the tile.

![Paint Y-axis](img/paint-2.gif)

Since the 3D cursor is an important part of the Sprytile workflow, you can ==move the 3D cursor== to the vertex nearest the mouse cursor by ==holding down the **`S`** key== while using Sprytile's tools.

![Cursor Snap](img/cursor-snap.gif)

Try reorienting the 3D view to face the last axis you have yet to paint on, then moving the 3D cursor by holding down the `S` key and moving your mouse. Paint on that axis. Note that the center of the grid has moved to where you have positioned the cursor.

![Paint X-Axis](img/paint-3.gif)

### Tile Grids

With the basics of building done, let's look at tile grids. Tilesets might be made up of tiles in different scales. To account for this, Sprytile allows you to paint tiles in different sizes. This part of the Sprytile panel allows you to create and organize the grid settings used with the tile map.

Press the `+` button at the panel and select the newly created entry. The settings for this new tile grid can be changed in the boxes below. For this tile grid, lets change it to a 16 x 16 tile size.

![Tile Grid Panel](img/tile-grid-panel.png)
![Tile Grid Editing](img/tile-grid-edit.png)

## Fill Tool

Looking closely at the last wall we created, we can see that the texture gets very repetitive. We'll use the smaller 16x16 tile grid we just made to break up the pattern.

Exit the build tool if you haven't done so yet, and delete the faces of wall we just created.

??? info "For Blender Newbies"

    To delete faces in Blender, go into the tweak/select tool by pressing `W`. Go into face mode by pressing the `3` key. Select the faces and delete them by pressing either `X` or `Del`, and then choosing faces.

    Bonus tip: holding down `shift` adds or removes to your selection. Holding `ctrl` will select the shortest path from your last selection to the new selection. Blender has powerful selection options worth exploring yourself.

To recreate the wall, we'll use the Sprytile fill tool. Select the fill tool from the toolbar, making sure the 16x16 grid is selected. The workplane has become bigger, indicating the area the tool will fill.

![Fill Tool](img/tool-fill.png)

The default fill size is a bit large, let's adjust it in the options to a more reasonable 6x4 grid. This part of the Sprytile panel is where the settings for Sprytile tools can be adjusted.

![Fill Grid Size](img/fill-grid-size.png)

As with other Sprytile tools, the fill tool is centered around Blender's 3D cursor. Holding the `S` key will snap the cursor to vertex nearest to the mouse, but there are no verts where we want to move the fill tool to. We can instead use the grid snap mode in the workflow panel.

![Cursor Snap Options](img/cursor-snap-options.png)

Set cursor snap to grid, and then hold down the `S` key to move the work plane with your mouse. Position the fill plane to where you want to build the wall, select the wall in the tile palette, and click inside the fill plane.

![Fill Tool](img/fill-tool-1.gif)

## Paint Tool

### Tile Flipping/Rotation ###



![Wall Small Tiles](img/wall-small-tiles.png)

But even with the smaller tiles, the repetition is still visible. With tile map editors, you can further break up the patterns by rotating and flipping tiles. To do that, we use this part of the Sprytile panel.

![Flip/Rotate Panel](img/flip-rotate.png)

The keyboard shortcuts for rotating tiles left and right are the `1` and `2` keys.

The `3` key toggles Flip X and the `4` key toggles Flip Y.

Repaint the wall using the tile flipping and rotation options.

!!! info "Tile Picker"

    You can pick tiles from your scene like in Photoshop. Hold down the `alt` key and select a tile from the scene with a left mouse click.

![Wall with tile rotations](img/wall-tile-rotation.png)

## Pixel Translate ##

This wall is placed in an awkward position. Sprytile makes moving faces easier in tile map mode by constraining movement to the pixel grid. Select the wall faces and split them by pressing the `Y` key. Now translate the selection by pressing the `G` key. The movement snaps to the pixel grid and a readout showing the movement is shown on the top left corner.

!!! info "Build Mode Automerge"

    It's necessary to split the faces because build mode automatically merges close vertices by default. You can turn off this option by toggling `Auto Merge` beneath the tile rotation/flip section.

![Pixel Rotation](img/pixel-translation.png)

Use the pixel translation tool to move the wall to a more sensible place. The movement is restricted along the work plane, so rotate the 3D view when necessary. Pixel translate is automatically used when in tile map mode.

![Moving the wall](img/wall-move.png)

!!! note "Snap Translate Vertices"

    By default, pixel translate will snap the selected vertices to the pixel grid around the 3D cursor. This can be turned off using the `Snap Translate` option in the Workflow panel.

## Paint Mode ##

Finally, we'll cover paint mode. Paint mode gives you tools to quickly UV map faces to tiles, allowing you to build your mesh with other Blender tools. Let's extrude the edges of the grass without using tile map mode so that the geometry isn't on the pixel grid anymore.

![Mesh Extrude](img/mesh-extrude.gif)

Next, turn on paint mode by pressing the `Paint` button in the Sprytile panel. Using the 32x32 tile grid, select the tile that is the border of the grass and the ground.

![Paint Mode Selected](img/paint-mode-select.png)

Now try painting the tile on one of the extruded faces. The texture appears stretched because of the current paint settings.

![Paint Mode Misalign](img/paint-mode-misalign.png)

Change the paint settings to the following and try painting the faces again.

![Paint Settings](img/paint-settings.jpg)

Now the grass/ground boundary appears because UV mapping of the face is being aligned to the top of the tile. Continue painting the other extruded faces.

![UV Aligned Painting](img/paint-aligned.png)

### Advanced Painting ###

Paint mode allows for easy UV mapping even when the face is not aligned to the global XYZ axis. Using the create tab, make a low poly
cylinder and rotate it so it is not aligned to the global XYZ axis.

![Create Tab](img/create-tab.png)

Switch to the 16x16 tile grid and select the following tile. Make sure that grid rotation is back at 0 and that Flip X and Y are off.

![Cylinder Creation](img/create-cylinder.png)

If you try painting the outer faces of the cylinder, you will notice that the alignment of the UV is not correct. To fix this, we can use hinting mode. Toggle on hinting in the Sprytile panel.

![Hinting Toggle](img/hinting-toggle.png)

Switch to edge selection mode and select one of the cylinder's edges along the long side. Then paint on the faces connected to the selected edge and notice that the UV mapping is now properly aligned to the face.

![Hinted Painting](img/hinted-painting.gif)

What hinting does is indicate to Sprytile which side of the face will be aligned to the horizontal axis of the tile map.

The cylinder still doesn't look like our selected tile. To fix this, we can use the stretch options on the paint tool.

![Stretch Options](img/stretch-options.png)

With the stretch options on, repeat painting the faces as with the previous step. Now the faces will be UV mapped with the selected tile stretched out over each face, looking more like the metallic pipe of the selected tile.

![Pipe Cylinder](img/pipe-cylinder.png)

## Conclusion ##

This tutorial gives an overview of Sprytile's basic functions, hopefully enough to help you to build cool things with it.

For more advanced uses of Sprytile, check the [Advanced Features](advanced-features) tutorial page.

If you have any questions, feel free to contact me on [twitter](https://twitter.com/chemikhazi) or via the [itch.io discussion boards](https://chemikhazi.itch.io/sprytile/community).
