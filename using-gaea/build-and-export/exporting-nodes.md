---
icon: sparkles
---

# Exporting Nodes

Gaea is primarily an asset generator designed for creating and exporting terrains to be used in other applications. It supports all major heightfield and mesh formats, ensuring compatibility with various platforms and rendering tools.

<figure><img src="../../.gitbook/assets/image (42).png" alt="" width="375"><figcaption><p>Output/Export Nodes in the Gaea Toolbox</p></figcaption></figure>

## **Output Nodes**

<div><figure><img src="../../.gitbook/assets/image (41).png" alt="" width="375"><figcaption><p>Mesher node properties</p></figcaption></figure> <figure><img src="../../.gitbook/assets/image (3).png" alt="" width="374"><figcaption><p>Export node for Bitmap export</p></figcaption></figure></div>

* **Node Types**: Utilize specific output nodes, such as Mesher for mesh generation, Point Cloud for simple XY point cloud export, or platform-specific nodes like [unreal-node.md](application-specific-export-nodes/unreal-node.md "mention") and [unity-node.md](application-specific-export-nodes/unity-node.md "mention"), to export your assets.
* **Customization**: Depending on the output node type, you can adjust settings such as map sizes for Unreal, file naming conventions, or mesh topology and vertex count for Mesher.
* **Naming Conventions**: The name of the exported file matches the name of the Output node, streamlining asset management and integration into other projects.

### **Mark for Export**

<figure><img src="../../.gitbook/assets/image (39).png" alt="" width="375"><figcaption><p>Data View's BUILD Tab showing nodes marked for export.</p></figcaption></figure>

* **Shortcut Key**: Right-click a node and select `Mark for Export` or press `F3` on any node to mark it for export. This flexibility allows you to export multiple node outputs simultaneously.
* **Build Tab and Settings**: The Build tab and Build Settings window display all nodes marked for export. Here, you can change the output format, select which ports to export, and rename the export files.
* **File Naming**: Exported files are named in the format `<Name or NodeName>_<PortName>.<extension>`, ensuring clarity and order in file management.

{% hint style="info" %}
You can disable `_Out` suffix for the Primary Port in [build-options](build-options/ "mention").
{% endhint %}

### Export Settings and Options

<figure><img src="../../.gitbook/assets/image (4).png" alt="" width="357"><figcaption></figcaption></figure>

**File name.** The node name is used by default for the export filename, however, you change the name in the Export Items list in the Build Tab in [data-editor](../../getting-started/user-interface/data-editor/ "mention") or in the [build-options](build-options/ "mention").

**File Formats.** Gaea supports a wide range of file formats, allowing you to choose the best option based on the requirements of the receiving application or your workflow needs.

**Port Selection.** From the export menu, you can select specific ports (such as Enabled, Out, Flow, Wear, or Deposits) to export, providing control over the data being exported and optimizing resource usage.

**Additional Options**

* **Primary Only.** Export only the primary or most important outputs of a node, reducing the number of files and focusing on key data.
* **Mark All/None.** Quickly select or deselect all available export options for efficiency and convenience.

{% hint style="info" %}
For automation scenarios where you wish to explicitly name the output file, see [managing-input-and-output.md](../../advanced-topics/automation/managing-input-and-output.md "mention") in [automation](../../advanced-topics/automation/ "mention")
{% endhint %}



