---
hidden: true
icon: x-ray
---

# Anatomy of Node

A Gaea node provides complex functionality packaged in a pre-built `Node` class that can be used to create your own nodes quickly and painlessly.

{% hint style="info" %}
This is a preview of an unreleased feature, and subject to change.
{% endhint %}



Let's take a look at the basic structure of a Gaea Node:

```csharp
import QuadSpinner.TOR.Framework;
import QuadSpinner.Gaea.Engine;
import QuadSpinner.Gaea.Engine.Framework;

namespace Daredevil.Nodes;

public class CustomNode : Node
{
    public CustomNode()
    {
        Name = "Custom Node";
        
        // Add second port. In/Out are always defined.
        Ports.Add(new Port("CustomInput", PortType.In | PortType.Required));
    }
    
    // Declare a Property and give it a Parameter attribute
    // to have it become visible in the UI
    [Parameter(0.5f, 0f, 1f)]
    public float Strength { get; set; } = 0.5f; // Give it a default value.
    
    [Parameter(Parameters.Seed)]
    public int Seed { get; set; } = Global.RandomSeed();
    
    // The main code where the input is processed and saved.
    public override void Build()
    {
        // Get a Map from the In port.
        Map map = In.GetData();
        
        if(map == null) throw ExHelper.RequiredNotConnected();
        
        // Classic loop
        for(int y = 0; y < map.Resolution.Height; y++)        
        {
            for(int x = 0; x < map.Resolution.Width; x++)
            {
                // add your processing code here
                map[x,y] = 1f - map[x,y];
            }
        }
        
        // Efficient lambda
        map.Process(x => Vector<float>.One - x);
        
        // Intrinsic functions with fluent syntax
        map = map.Invert()
                 .Autolevel()
                 .Shaper(-0.5f)
                 .Warp(0.5f, 0.2f, Seed)
                 .Clamp(0.3f, 0.7f);
                 
        map *= (Noises.Perlin(0.5, Seed + 5) * 0.3);
        
        // Cache the processed data.
        Commit(map);
    }

}
```

You can use many powerful and efficient low-level functions such as Autolevel, Clamp, Blur, etc. These methods are part of the Engine and built with extremely fast processing code.

If you wish to use C++ for processing, you can P/Invoke your C++ code from the `Build()` method.
