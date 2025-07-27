# Using Modifiers

<figure><img src="../../.gitbook/assets/image (26).png" alt="" width="375"><figcaption></figcaption></figure>

## Modifiers

The Modifier Stack provides quick access to common adjustments, masks, and modifications that you may wish to apply to a node. Traditionally, node-based software would require you to create an additional node for each such adjustment - often resulting in complicated graphs that are difficult to manage.

For basic information about Modifiers, see [modifier-stack.md](../../getting-started/user-interface/property-editor/modifier-stack.md "mention")

### Fast and Less Overhead

Modifiers work as a post-process so updating them does not require re-building the node. And unlike nodes, Modifiers don't create excess overhead. The memory cost of 6 modifiers is the same as 1 modifier, however the cost of 6 nodes of the same types would create 6 times the overhead.

## Common Scenarios

### Adjusting the Height

If a terrain (or mask) is not the exact height values you need, you can use the Height Remap modifier to adjust both the lower and upper extent of your terrain. Bringing up the bottom "raises" the terrain from the bottom, while "lowering" the top makes the terrain shorter.

<figure><img src="../../.gitbook/assets/image (65).png" alt="" width="314"><figcaption></figcaption></figure>

Inversely, bringing the top beyond 1.0 makes your terrain taller than the original range.

### Making Stronger Masks

By simply applying Autolevel, Equalize, or Shaper (positive value) you can take a weak mask and make it stronger.

<div><figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure></div>

### Dropping the Terrain

The "Drop" modifier removes any "empty" space under the terrain, forcing it to drop to the "floor".

<figure><img src="../../.gitbook/assets/image (68).png" alt="" width="316"><figcaption></figcaption></figure>

<div><figure><img src="../../.gitbook/assets/Gaea_-_Untitled_02-55-12-AM.jpg" alt=""><figcaption><p>Normal Perlin</p></figcaption></figure> <figure><img src="../../.gitbook/assets/Gaea_-_Untitled_02-55-15-AM.jpg" alt=""><figcaption><p>Dropped Perlin</p></figcaption></figure></div>

### Bulking Up or Bulking Down

Using Shaper, you can bulk up or bulk down a terrain. It can apply to masks as well. For example, taking Flow Map output and making it stronger by adding Shaper.

<figure><img src="../../.gitbook/assets/Gaea_-_Untitled_02-52-42-AM.jpg" alt=""><figcaption><p>Original terrain</p></figcaption></figure>

<div><figure><img src="../../.gitbook/assets/Gaea_-_Untitled_02-52-58-AM.jpg" alt=""><figcaption><p>Shaper at +50</p></figcaption></figure> <figure><img src="../../.gitbook/assets/Gaea_-_Untitled_02-52-51-AM.jpg" alt=""><figcaption><p>Shaper at -50</p></figcaption></figure></div>

### Restrict Effect to Slope or Height

You can easily restrict the effect of a node to a height or slope range by adding a "Mask by Height" or "Mask by Slope" modifier on the effect node.

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (66).png" alt="" width="313"><figcaption></figcaption></figure>

{% hint style="info" %}
You can attach a DataExtractor node to any node that uses a Mask by Height/Slope modifier, and get the exact mask generated as a separate output.
{% endhint %}

### Using Min and Max

The Min and Max modifiers are one of the most powerful tools in Gaea.

### Breaking up a Mask

Sometimes you want a bit of crunchy detail to breakup the edges of your mask or introduce some uneven variations. Add a Warp modifier with the appropriate Size and Strength to change the mask.

<figure><img src="../../.gitbook/assets/image (69).png" alt="" width="314"><figcaption></figcaption></figure>

<div><figure><img src="../../.gitbook/assets/threshold1.jpg" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/threshold2.jpg" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Try mixing with Min or Max modifiers for broader options.
{% endhint %}

### Getting the Difference

