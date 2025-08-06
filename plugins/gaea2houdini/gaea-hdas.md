# Gaea SOP Nodes

## Gaea Terrain Processor (SOP Node)

The **Gaea Terrain Processor** node runs `.terrain` files authored in Gaea 2.2 or newer. These terrain files can include exposed parameters, input bindings, and output maps. The node executes Gaea Swarm in the background and caches results locally on disk.

### **Key Features**

* Runs `.terrain` files inside Houdini SOP networks.
* Supports exposed parameters, input bindings, and output maps.
* Automatically caches results to disk to avoid redundant recomputes.
* Can be used with PDG, loops, and other procedural workflows.

### **Parameters**

* **Gaea 2.2 Terrain File**\
  Path to the `.terrain` file containing your Gaea graph with exposed inputs/outputs.
* **Generate Parameters**\
  Reads the file and generates the appropriate UI in Houdini to control Gaea parameters and I/O.
* **Cook**\
  Manually triggers execution of the terrain file and refreshes the cache.
* **Auto Cook**\
  Automatically triggers a recook when inputs or parameters change. Disable to rely solely on the disk cache.

### **Advanced Parameters**

* **Extra Data**\
  Adds a unique string to the cache ID. Essential when using PDG or ForEach loops to avoid cache conflicts.
* **Cache Directory**\
  Specifies where the terrain output cache is stored. Deleting this will force a recook.
* **Custom Gaea.SwarmHost.exe**\
  Lets you manually define the path to the SwarmHost executable. If disabled, Houdini uses the path from the system registry.

***

## Gaea Terrain Color Visualizer (SOP Node)

The **Gaea Terrain Color Visualizer** simplifies the process of viewing color maps or masks on your Gaea terrain output within Houdini’s viewport.

### **Why it’s useful**

Houdini uses the same mechanism to display both color and masks, making it hard to switch between them. This node gives you convenient control over visualization.

### **Parameters:**

* **Visualize**\
  Choose what to view in the Houdini viewport:
  * **Terrain Color**: Shows RGB terrain data, e.g. `color.r`, `color.g`, `color.b`.
  * **Regular Mask**: Displays the default mask channel.
* **Channels**\
  When using _Terrain Color_, this defines which attributes to use for R, G, and B. With Gaea outputs, these are typically `color.r`, `color.g`, `color.b`.

