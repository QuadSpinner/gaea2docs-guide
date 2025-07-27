# Erosion\_1

<figure><img src="https://docs.quadspinner.com/images/ref/Erosion/Erosion--Default.webp" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
This page refers to Erosion, aka Erosion\_1 or Classic Erosion. It was the mainstay of Gaea 1.0's erosion toolkit, and is also available in Gaea 2.0.

[erosion\_2](erosion_2/ "mention")is the newer generation of Erosion and provides new options and dramatically higher performance. The general principles of Erosion\_1 still apply to Erosion\_2.

Both nodes can be used side-by-side for leveraging their unique abilities.
{% endhint %}

**Selective Processing**

While the Erosion node can be masked using the standard masking process, the Area mask input gives you additional options.

When an Area mask is connected, you can control the Rock Softness, Precipitation, or Erosion Strength. Unlike the standard mask, the Area mask allows the processing to be masked but not the shape. For example, you can mask out the top part of a volcano and choose Precipitation as the Area Effect. This forces the erosion-inducing precipitation to occur only within the masked area. But the resulting erosion can flow out and affect the rest of the terrain.

For more information, see Selective Processing in Erosion node details.

**Layering Erosion**

Erosion can give you even more complex results when used multiple times.

A great way to create sophisticated erosion is to use multiple Erosion nodes. A single erosion pass is fine, but will restrict you because of the settings you can use.

In this example, we have `Selective Processing` set to `Altitude` with high `Duration` of `30%` for creating the initial pass. The strong grooves/flow structure it creates will guide the erosion in subsequent passes.

<figure><img src="https://docs.quadspinner.com/images/ref/Erosion/Erosion-Pass1.webp" alt=""><figcaption></figcaption></figure>

For the second pass, we have default settings except for `100%` `Downcutting` and `100%` `Base Level`. This creates strong flow structures everywhere.

<figure><img src="https://docs.quadspinner.com/images/ref/Erosion/Erosion-Pass2.webp" alt=""><figcaption></figcaption></figure>

The third pass is fully default. It takes the general larger variations created in the previous passes and homogenizes the overall "texture" yet keeps the larger features. Optionally, higher Inhibition can be used to create more sediments at the bottom.

<figure><img src="https://docs.quadspinner.com/images/ref/Erosion/Erosion-Pass3.webp" alt=""><figcaption></figcaption></figure>

**Data Output**

The Erosion and Wizard nodes create 3 key data outputs:

| Data     | Description                                                                             |
| -------- | --------------------------------------------------------------------------------------- |
| Wear     | The portions where erosion removes sediments.                                           |
| Deposits | The resting position of those sediments.                                                |
| Flow     | The path of the sediments from their original location to their final resting position. |

These maps can be used for texturing or for driving other nodes.

TIP

Like other data maps, the output may not be readily visible to the human eye. You can use Adjust to autolevel or equalize the output. You can also use Threshold to create a solid mask.

NOTE

In digital terrains, inexperienced artists will often try to use the Flow output too prominently for texturing. While this may work in some situations, it tends to create unrealistic textures and can make your terrain look fake and "CG". See the Misconceptions section below.
