# Using Existing Tilesets

By using [tilegrid settings](advanced-features#additional-tile-grid-settings), Sprytile can use existing 2D tilesets assets but some care should be taken in how you use them.

## Power of Two Texture Sizes

The importance of Power of Two texture sizes is discussed in detail in [creating tilesets](creating-tilesets#power-of-two-sizes).

If you wish to use your scenes in a game engine, you will likely need to resize the tileset you want to use so that it is a power of two size.

The easiest way to do this is to expand the canvas size so that it becomes a power of two size. The downside is that this is a wasteful use of texture space in 3D engines.

The recommended method that takes more work is to remove tiles from the tileset that will not be used, or to split the tileset into multiple textures that are power of two sized.

## UI considerations

Related to the texture sizes, the Sprytile UI was not designed with existing tile sets in mind. Most 2D asset packs put every tile into one texture which makes them difficult to use with Sprytile.

As above, consider splitting big asset packs into smaller textures in an image editor for ease of use in Sprytile.