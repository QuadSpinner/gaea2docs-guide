# Property Editor Toolbar

Property Editor Toolbar in placed on top of Property Editor. It provides various options related to the selected node in graph.

<figure><img src="../../../.gitbook/assets/Property Editor Toolbar.png" alt="" width="375"><figcaption><p>Property Editor Toolbar</p></figcaption></figure>



Replace Node: This dropdown menu lists nodes related to the currently selected node. Selecting an option will replace the current node with the chosen one. The "Other node" option allows users to search and replace the current node with any other node available.

State Management: This dropdown provides various options to manage selected node state.

<figure><img src="../../../.gitbook/assets/Property Editor StateManagement.png" alt="" width="227"><figcaption><p>State management</p></figcaption></figure>

* **Revert Changes**: Undo recent modifications and return the selected properties to their previous state.
* **Reset to Defaults**: Restore the default settings for the selected properties.
* **Save State**: Saves the current settings of the selected properties for later retrieval. Once clicked, this option transforms into "Load State," which can be used to reload the previously saved settings.

Toggle Gizmo: Activates when a node supports gizmo functionality. When enabled, it displays the gizmo for the selected node in the 3D viewport.

<figure><img src="../../../.gitbook/assets/Toggle Gizmo.png" alt="" width="38"><figcaption></figcaption></figure>

Property Editor submenu: offers a suite of options that allow users to fine-tune the behavior and appearance of selected nodes within the project.

<figure><img src="../../../.gitbook/assets/Property Editor Submenu.png" alt="" width="227"><figcaption><p>More options</p></figcaption></figure>

**Render Intent (Override) Submenu** This submenu allows users to customize the rendering behavior of the selected node in the viewport. Options include:

* **Default**: Utilizes the node's standard rendering.
* **Heightfield**: Interprets the output as a height map, ideal for terrain visualization.
* **Mask**: Renders the output as a mask.

Presets: This option allows users to create and apply presets for the current node. Presets can be managed and selected from the preset submenu to quickly configure node settings. See [presets.md](../property-editor/presets.md "mention")

Show Help for this Node: It opens documentation page for the selected node.

Node-specific commands are accessible via the Property Editor toolbar. The accompanying image illustrates the toolbar for a combine node, highlighting two available command buttons: "Switch Inputs" for rearranging the node inputs and "Add Input" for introducing additional input.

<figure><img src="../../../.gitbook/assets/Property Editor Commands.png" alt="" width="375"><figcaption><p>Node specific commands</p></figcaption></figure>
