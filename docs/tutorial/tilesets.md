# Tilesets and Sprytile

Before getting started with using Sprytile, we'll discuss limitations you should be aware of when creating or using textures for 3D.

## Power of Two textures

When working with 3D, it is recommended that textures should be in **Power of Two** sizes.

In the simplest terms, power of two sizes means that textures should have widths and heights that are any of the following pixel sizes:

!!! note "Power of Two Sizes"

	**8, 16, 32, 64, 128, 256, 512, 1024, 2048, 4096**

Textures do not have to be square but can be any combination of the above sizes, for example 32x64.

The technical reasons for using power of two sizes is beyond the scope of this tutorial, but certain 3D engines may cause rendering artifacts when using Non Power of Two (**NPOT**) textures.

Blender's internal rendering engine is capable of handling NPOT textures, but if you plan on using your creations outside Blender it is safer to start with Power of Two sizes for your tilesets.

## Using Asset Packs

By using [tilegrid settings](../advanced-features#additional-tile-grid-settings), Sprytile can use existing 2D tilesets assets.

However, many of these files are not designed with 3D in mind and may not come in power of two sizes.