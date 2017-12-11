# Tilesets and Sprytile

Before starting to use Sprytile we'll discuss tilesets, which are an important concept for Sprytile.

Tilesets are image files containing multiple tile sprites. In old games, these were used to build 2D levels. In Sprytile, we use the same concept but to build in 3D.

You can either create a tileset from scratch or use existing asset packs. Either way, you should be aware of some limitations with using images as textures in 3D. 

!!!note "Textures"

	When working in 3D, image files are called textures.

## Power of Two Texture Sizes

When working with textures in 3D, it is recommended that textures should be in **Power of Two** sizes.

In the simplest terms, power of two sizes means that textures should have widths and heights that are any of the following pixel sizes:

!!! note "Power of Two Sizes"

	**8, 16, 32, 64, 128, 256, 512, 1024, 2048, 4096**

Textures do not have to be square but can be any combination of the above sizes, for example 32x64. 
The technical reasons for using power of two sizes is beyond the scope of this tutorial, but certain 3D engines may have rendering artifacts when using Non Power of Two (**NPOT**) textures.

Blender's internal rendering engine is capable of handling NPOT textures, but if you plan on using your creations outside Blender it is safer to start with Power of Two sizes for your tilesets.

## Using Asset Packs

Asset packs are textures that are available for free or for sale that you can use to build a game with. Most tileset assets were created with 2D in mind, but it is still possible to modify or use them as is in Sprytile.

By using [tilegrid settings](../advanced-features#additional-tile-grid-settings), Sprytile can use existing 2D tilesets assets. You will have to adjust these settings according to the tileset you are using.

However, these assets may not be designed with 3D in mind and the textures might not come in power of two sizes.

### Modifying NPOT Assets

If you will be using your models in a 3D engine that does not support NPOT textures, you will have to modify the textures that come from NPOT assets.

The easiest way to do this is to expand the canvas size so that it becomes a power of two size. The downside to this method is the waste of texture space in 3D engines.

The recommended method that takes more work is to remove tiles from the tileset that will not be used, or to split the tileset into multiple textures that are power of two sized.