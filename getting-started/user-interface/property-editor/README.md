# Property Editor

## Modifying Properties

Every node exposes a set of properties or settings that you can modify to influence the effect that node has on the terrain. When you select a node, the settings become available in the Properties panel in the right side of the interface.

When you change a property, the effect is immediately applied and made visible in the viewport. Most nodes have a limited type of properties:

* **Integer**: such as `1`, `2`, `3`, `4`, etc. They usually define quantity or a finite value, like angle.
* **Decimals**: such as `0.1`, `0.256`, `0.4885`, etc. They usually define the strength or amount of a certain setting. In most cases, small changes can be quite powerful.
* **Toggle**: They usually allow you to turn a feature on and off.
* **Choices**: These take the form of a dropdown where you can select one of many options.
* **Color**: They allow you to choose a color for the color production nodes.
* **File**: They allow you to choose a file from your computer.

Sliders with unmodified (default) values are shown with slightly muted colors. This can be controlled through [options.md](../../options.md "mention").

Some nodes may have unique controls specific to them.

{% hint style="info" %}
One of the easiest ways to learn about a node's properties is to experiment. Try different values across the range for each property to observe the effect they have.
{% endhint %}

{% hint style="warning" %}
If a setting says "Iteration", "Strength", "Cycles", or "Amount", be cautious. High values may take longer to process.
{% endhint %}



### Editing Values <a href="#modifying-values" id="modifying-values"></a>

For properties that allow numeric entry (Integer or Decimals), you can right-click the property and enter a number.

### Entering Values in Metric

For values shown as percentages, you can enter a value in meters and Gaea will convert it to the appropriate percentage or decimal value proportionate to the metric value in relation to the Terrain Definition set in the Build tab.

For example, if you enter `500m` and your Terrain width in [build-options](../../../using-gaea/build-and-export/build-options/ "mention") > [#terrain](../../../using-gaea/build-and-export/build-options/#terrain "mention") is set to `5000m` the value will be converted to `(500m / 5000m)` - in other words, it will be `0.1` or `10%` as appropriate.

### Nudge Popup

The Nudge panel is available when you right-click an Integer or Decimals property. With the Nudge panel, you can achieve much higher precision in entering values.

| Command        | Description                                  |
| -------------- | -------------------------------------------- |
| Halve          | Halves the current value.                    |
| Double         | Doubles the current value.                   |
| Minimum        | Uses the lowest allowed value.               |
| Decrease Large | Decreases by a large value. (ex: 10 in 100%) |
| Decrease Small | Decreases by a small value. (ex: 1 in 100%)  |
| Reset          | Resets to the original / default value.      |
| Increase Large | Increases by a large value. (ex: 10 in 100%) |
| Increase Small | Increases by a small value. (ex: 1 in 100%)  |
| Maximum        | Uses the highest allowed value.              |

### **Seed Reset**

Seed Reset is a minor enhancement in the Nudge UI. It sets the “Default” seed value to whatever the random value is when the node is created. So if you play around for a while and want to go back to the original seed, you can simply reset the Seed.
