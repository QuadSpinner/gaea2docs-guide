# Visualizing Scale

## Using Overlays

Gaea 2.1 ships with multiple pre-defined overlays that you can use for showing relative scale on your terrain. These are rendered on top of your terrain, so you can visualize it easily without modifying anything on your graph. You can change the overlay and its opacity in the Sky Editor.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

{% include "../../.gitbook/includes/this-feature-is-to-be-intro....md" %}

A great way to visualize specific scale is to create your own overlay with precise shapes and sizes.

### Creating a custom Overlay

You can load a custom Overlay in the Viewport Sky Editor.

To craft precise shapes in an overlay, you can use the following simple formula.

If your overlay is 2048 x 2048, then 2048 = 2500m (or whatever your [Terrain Width](../../advanced-topics/technical-information/dimensions-and-scale.md#terrain-size-and-height) is set in Gaea). Then `1m = 2048 / 2500m` (ie, `0.8192`). For 25m, you use `0.8192 x 25 = 20.48` so create a square in your design application that is 20.48 x 20.48 px in size and place it where you wish. 50m would be 40.96, and so on.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

Save your square image as a PNG to maintain crisp edges. Then load it as a custom overlay in Gaea.

Now you can visualize any specific area, shape, perimeter, etc. on your terrain.

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

### Creating Overlays in Gaea

Use an app like [Lunacy](https://icons8.com/lunacy?ref=quadspinner), Figma, Illustrator, etc. to create a custom overlay. However, if you want to skip using external apps, you can easily create a simple overlay in Gaea.

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

Create a Constant setup like explained above. Then add a Curvature node, and set it to Vertical mode with 100% Falloff. This will create an outline for your cube.

<figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

You can optionally invert the output as Gaea's overlay is multiplied on top of your existing render. Once your visual is ready, right-click the 2D Viewport and select `Save to File` to save the file which you can use a custom overlay.

You can create more elaborate overlays by using Grid, Halftone, Tint, and various other nodes.

<figure><img src="../../.gitbook/assets/image (20).png" alt="" width="563"><figcaption></figcaption></figure>

## Creating a 3D Scale Dummy

This technique will show you how to create a simple cube/block of a specific scale that you can add to your terrain preview.

First we create a `Constant` node and set its value to 1.0. Then connect it to a `Transform` node.

<figure><img src="../../.gitbook/assets/image (6).png" alt="" width="375"><figcaption></figcaption></figure>

In the Transform node, right-click Scale and enter a metric value such as `25m`. This will scale the Constant into a perfect 25 x 25m block. Additionally, you can add a `Height Remap` modifier and scale the block vertically to any specific size in the same way.

<div><figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure></div>

Now you have this scale block.

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

If you want to view it on your terrain, create a Combine node to Add this block on top of your terrain.

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

If you want to toggle this block and use it frequently in various places across your graph, you can use the Route utility node. Feed your main terrain into the `In` port and the Combined block output to the `Alternate` port.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption><p>Setup a Route node to conveniently hide the block when not needed.</p></figcaption></figure>

You can use the Route node's toggle to quickly show and hide the version with the Block.

<div><figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption><p>Route toggled on.</p></figcaption></figure> <figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Route toggled off.</p></figcaption></figure></div>

{% hint style="info" %}
Make the Transform's output into a [Portal](portals-and-chokepoints.md) and reuse it wherever needed in the graph without cluttering the workspace.
{% endhint %}

### Creating a Custom Reference Object

If you want to use a custom mesh instead of a block, you can use the Object node to import a mesh and scale it instead of using the Constant node.

<figure><img src="../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

