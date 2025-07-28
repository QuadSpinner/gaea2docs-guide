# Working with SatMaps

Our library of over 1400 color maps, derived from real satellite data, helps you colorize your terrains quickly without sacrificing realism.

<figure><img src="../../.gitbook/assets/SatMap.png" alt="" width="314"><figcaption></figcaption></figure>

This tech was originally pioneered by QuadSpinner for GeoGlyph in 2014, Gaea's latest iteration provides an extensive library covering all natural locations, giving you a vast playground for colorizing your terrains.



<div><figure><img src="../../.gitbook/assets/Gaea_-_Untitled_03-22-12-AM.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/Gaea_-_Untitled_03-22-15-AM.png" alt=""><figcaption></figcaption></figure></div>

This TextureMap node is attached to a SatMap node. The SatMap is adapted to the mask as described in [crafting-masks.md](crafting-masks.md "mention").

## Editing SatMaps

There a few ways to quickly tweak the SatMaps to better fit your needs.

### Map Bias

By moving the Bias slider, you can have the SatMap apply more towards the left (negative values) or right (positive values) of the selected Color Map.

| <div><figure><img src="../../.gitbook/assets/Gaea_-_Untitled_03-23-29-AM.png" alt=""><figcaption></figcaption></figure></div> | <div><figure><img src="../../.gitbook/assets/Gaea_-_Untitled_03-23-39-AM.png" alt=""><figcaption></figcaption></figure></div> | <div><figure><img src="../../.gitbook/assets/Gaea_-_Untitled_03-23-51-AM.png" alt=""><figcaption></figcaption></figure></div> |
| ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| <div><figure><img src="../../.gitbook/assets/satmap_bias_none.png" alt=""><figcaption></figcaption></figure></div>            | <div><figure><img src="../../.gitbook/assets/satmap_bias_low.png" alt=""><figcaption></figcaption></figure></div>             | <div><figure><img src="../../.gitbook/assets/satmap_bias_high.png" alt=""><figcaption></figcaption></figure></div>            |

### Map Clipping

You can use the Clip slider to tell SatMaps to only use the selected segment of the entire color map.

<figure><img src="../../.gitbook/assets/Gaea_-_Untitled_03-23-01-AM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/satmap_clipping.png" alt="" width="291"><figcaption></figcaption></figure>

Here, we clip out most of the left half of the color map, and you can see how that changes the influence of the color map on the terrain.

#### Roughness

The Roughness setting scatters the pixels of the color map to add the desired level of chaos and distortion.

<div><figure><img src="../../.gitbook/assets/Gaea_-_Untitled_03-35-36-AM.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/Gaea_-_Untitled_03-35-39-AM.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/Gaea_-_Untitled_03-35-41-AM.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/Gaea_-_Untitled_03-35-44-AM.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/Gaea_-_Untitled_03-35-47-AM.png" alt=""><figcaption></figcaption></figure></div>

#### HSL

The final tweaks come from Hue/Saturation/Luminosity editing.

***

SatMaps are one of the crucial aspects of colorizing your terrains. You can elevate your SatMaps by combining them with a Mixer as explained in [layering-textures.md](layering-textures.md "mention").

And finally, add [colorerosion.md](colorerosion.md "mention") to add a new level of realism to your texture maps.
