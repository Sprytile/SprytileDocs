# Creating Tilesets

These are high level guidelines for creating tilesets and is not a tutorial for how to create tile sets.

## Power of Two Sizes

Blender and Sprytile are working with 3D models and thus have the limitations associated with 3D.

One of these limitations is the recommendation that textures should be in **Power of Two** sizes.

In the simplest terms, power of two sizes means that textures should have widths and heights that are any of the following pixel sizes:

!!! note "Power of Two Sizes"

	**8, 16, 32, 64, 128, 256, 512, 1024, 2048, 4096**

While Blender's own renderer can handle non Power of Two textures, many real time renderers may have issues with using non Power of Two textures which can lead to a blurry look.

It is highly recommended to stick to these sizes when creating tilesets for use with Sprytile.

If you wish to find out more about the technical details of power of two textures, this is a [good primer](https://www.katsbits.com/tutorials/textures/make-better-textures-correct-size-and-power-of-two.php) to read.

## High Resolution Tilesets

While theoretically possible, high resolution tiles sets have not been tested yet. There is a high likelihood that you will need to use [advanced tile grid settings](advanced-features/#additional-tile-grid-settings) and use padding to [avoid texture bleeding](https://itch.io/t/72048/suggestion-for-accomodating-bleeding-fix).