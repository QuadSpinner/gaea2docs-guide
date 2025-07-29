# Debris

Simulate mechanical erosion with thousands (even millions) of individual, physical rocks and other geological debris using our physics-engine powered Debris simulation.

<figure><img src="../../.gitbook/assets/Gaea_-_TalusNode003.terrain_11-54-53-PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Gaea_-_TalusNode003.terrain_11-57-19-PM.png" alt=""><figcaption></figcaption></figure>

You can keep them in the heightmap, or export a point-cloud for later use. You can even color each rock individually.

<figure><img src="../../.gitbook/assets/debrismask.webp" alt=""><figcaption></figcaption></figure>

### Emission Source

The Debris simulation lets you control the emission source so you can place the debris as needed. In this image, the flow map of the terrain is provided as the Emitter Source, so the debris form only within those lanes and the take advantage of the inherent physics of the flows to create scree rivers.

<figure><img src="../../.gitbook/assets/Gaea_-_cx1.terrain_06-47-11-AM - Copy.jpg" alt=""><figcaption></figcaption></figure>

## Friction and Restitution

The Friction and Restitution controls determine how debris behaves when it falls and slides across the terrain. While we often describe it as controlling how far debris can travel, in the underlying physics, it’s about **energy loss** during movement:

* **Restitution**: Energy lost during impacts – how far debris bounces or slides after hitting a surface.
* **Friction**: Energy lost while sliding – how easily debris moves across the terrain.

So, adjusting friction changes how steep or shallow debris deposits will appear in your terrain simulations. Higher friction = steeper, shorter slides. Lower friction = longer, shallower debris spreads.

{% hint style="info" %}
For natural rock surfaces, the friction coefficient averages around **0.62**. This value directly relates to the **slope of repose** – the stable angle at which debris piles up. A friction coefficient of 0.62 corresponds to a **32° slope**, which is the typical angle of a talus (debris pile) formed under gravity.
{% endhint %}

### Size, Shape, and Layering

You vary debris sizes and even layer multiple Debris simulations to mix and match settings and shapes. The Debris node provides Sharp and Round rock shapes.

<figure><img src="../../.gitbook/assets/Gaea_-_TalusNode002.terrain_09-02-33-PM - Copy (1).jpg" alt=""><figcaption></figcaption></figure>

See the Debris examples that ship with Gaea to see how layering multiple simulations work.

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
When using multiple Debris nodes, you can use [accumulators.md](../managing-graphs/accumulators.md "mention") to combine all the output masks for colorization and other purposes.
{% endhint %}

