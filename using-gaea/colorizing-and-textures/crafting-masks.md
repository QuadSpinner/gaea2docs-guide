# Crafting Masks

## What is Color Lookup/CLUT?

All color texture generation in Gaea relies on applying color ramps (gradients) through a black-and-white mask.

A simple example: the darkest part of the gradient maps to the lowest terrain elevations, while the brightest part maps to the highest. Intermediate grayscale values distribute the gradient proportionally. This is known as a CLUT or Color Look Up Table.

<figure><img src="../../.gitbook/assets/CLUTer.png" alt=""><figcaption></figcaption></figure>

In this example, the gradient from a CLUTer node is mapped directly to the heightfield.

<figure><img src="../../.gitbook/assets/mountain_autolevelled.png" alt=""><figcaption></figcaption></figure>

Now, let's a try more detailed, colorful gradient.

<figure><img src="../../.gitbook/assets/Gaea_-_Untitled_04-39-07-AM.png" alt=""><figcaption></figcaption></figure>

You can see how it distributes across the terrain.

<figure><img src="../../.gitbook/assets/Gaea_-_Untitled_04-38-54-AM.png" alt=""><figcaption></figcaption></figure>

Now, if you use the same CLUT map but feed it a FlowMap instead of the terrain height, the texture will follow the flow lines defined by the FlowMap, producing a very different result.

<figure><img src="../../.gitbook/assets/Gaea_-_Untitled_04-39-18-AM.png" alt=""><figcaption></figcaption></figure>



### Colorization with Texture Nodes

Gaea provides nodes such as [TextureBase](https://app.gitbook.com/s/QDbwutRMkOIUKbLVMSQP/nodes/derive/texturebase "mention") and [Texturizer](https://app.gitbook.com/s/QDbwutRMkOIUKbLVMSQP/nodes/derive/texturizer "mention") provide complex colorization masks based on the terrain's inherent features.

<figure><img src="../../.gitbook/assets/Gaea_-_Untitled_04-44-21-AM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Gaea_-_Untitled_04-47-53-AM.png" alt=""><figcaption></figcaption></figure>

Which can create more complex textures such as this:

<figure><img src="../../.gitbook/assets/Gaea_-_Untitled_04-50-15-AM.png" alt=""><figcaption></figcaption></figure>



## Data Maps

Data Maps are specialized masks for selecting key terrain properties like slope, angle, and curvature, or for generating complex simulation-based data such as water flow and soil deposits. Additional maps like TextureBase produce pseudo-random texture masks for quick, easy color texturing.

Unlike the classic approach that combines basic data (slope, angle) with noise (e.g., Perlin) or depends heavily on erosion flow outputs—often requiring careful seed tuning—Data Maps introduce controlled randomness derived from systematic terrain analysis. This produces more natural, believable color maps.

### Aspect Maps

Aspect Data Maps mask out aspects of the terrain such as Height, Slope, Curvature, Angle, Peaks, etc.

<figure><img src="../../.gitbook/assets/datamaps.webp" alt=""><figcaption></figcaption></figure>

### Generative Maps

Generate Data Maps run various algorithms on the terrain to generate information such as Flows, Soil, Rock Occlusion, etc.

<figure><img src="../../.gitbook/assets/datamaps2.webp" alt=""><figcaption></figcaption></figure>

Data Maps can be combined together or with Texture nodes to create complex texture masks for colorization.

