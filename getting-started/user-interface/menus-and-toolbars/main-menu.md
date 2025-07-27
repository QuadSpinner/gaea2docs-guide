# Main Menu

## File Menu

* **New**: Start a new project.
* **Open**: Open an existing project file.
* **Open Recent**: Access recently opened files.
* Start Dialog: Opens the start dialog.
* **Save**: Save current project.
* **Save As**: Save project under a new name.
* **Save Incremental**: Save a versioned copy of the project.
* **Repair File**: Attempt to fix corrupted files.
* **Import**: Bring external files into the project.
* **Export**: Save parts of the project in various formats.
* **Share**: Share project through specified methods.
* **Exit**: Close Gaea.

## Edit Menu

* **Undo**: Revert the last action.
* **Redo**: Reapply the last undone action.
* **Cut**: Remove selected nodes and copy to clipboard.
* **Copy**: Copy selected nodes to clipboard.
* **Paste**: Insert nodes from clipboard.
* **Copy Properties**: Copy properties of selected node.
* **Paste Properties**: Apply copied properties to another node.
* **Rename**: Rename the selected node.
* **Duplicate**: Create a copy of the selected node(s).
* **Delete**: Remove selected item(s) from the graph.

## Graph Menu

* Add Note: Adds a note object to graph surface.
* Zoom: Zoom options.
* Selection: Zooms to fit the selected nodes within the view.
* Extents: Zooms to display all nodes.
* Reset Zoom: Resets the zoom level to the default view.
* Save Screenshot: Save graph screenshot.
* Screenshot Options: Options to save Graph, Viewport Screenshot and open screenshot folder.
* Show Grid: Toggle the visibility of the grid overlay on the graph.
* Snap to Grid: Enable or disable alignment of items to the grid lines.
* Snap to Items: Toggle whether items snap to align with other items on the graph.
* Baking:
  * **Bake Selected**: Bakes the selected nodes.
  * **Bake Required Nodes**: Caches all nodes necessary for the current operation.
  * **Force Load Baked Cache**: Loads all cached data forcibly.
  * **Unbake Selected**: Unbakes the selected nodes.
  * **Unbake All**: Clears all cached data.
  * **Resolution**: Allows setting the cache resolution, with options including 1024x1024, 2048x2048, 4096x4096, and 8192x8192.
  * **Cache to Disk**: Enables caching data to disk for persistent storage.
  * **When Closing File**: Determines cache behavior when the project file is closed.
  * **When Idle**: Controls cache behavior when the system is idle.
  * **Delete Cache**: Removes all cached data permanently.
* Bookmarks: Allows users to bookmark the current node. Bookmarked nodes are listed in the Bookmarks menu. Clicking a bookmarked node navigates directly to that node in the graph.



## Node Menu

* **Refresh**: Reload node content.
* **Bypass**: Temporarily disable a node.
* **Lock Preview to Node**: Set preview exclusively to selected node.
* **Mark for Export**: Designate node for export.
* **Reset**: Reset node to default state.
* Mutate: Mutate the current node.
* **Locked 2D Viewport**: Toggle lock for 2D viewport display.
* **Select**: Select nodes.
* **Upstream**: Select all nodes upstream.
* **Downstream**: Select all nodes downstream.
* Group/Ungroup: Create a group for selected Nodes. If a group is selected, it ungroups the nodes.
* Combine nodes: Combines the selected nodes.
* Convert port to portals: Select an output port from the list to convert it into a portal.
* Move to Tab: Select from a list of graph tabs to move the current node to your chosen tab.
* **Presets**: Access saved node presets.

## Preview Menu

* **Resolution**: Set project resolution (e.g., 512x512 to 4096x4096).
* **Regions**: Define regions for selective processing.
* **Engine Active**: Toggle engine processing.
* **Clean Memory**: Free up allocated memory.
* **Clear Cache**: Clear cached data.
* **Rebuild All**: Rebuild the project from scratch.
* **Build HD Preview**: Generate a high-definition preview of the terrain. (Coming Soon)
* Record Turntable Animation: Create a turntable animation by setting the frames and resolution.

## Project Menu

* **Build and Export**: Build project and export assets.
* **Queue Batch Build: Execute multiple builds in a queue using build profiles.**
* **Queue Network Build**: Add build to network queue.
* **Build Settings**: Configure build parameters.
* **Build Stack**: Manage build history and stacks.
* **Open Build Folder**: Open directory with build files.
* **Reports**: View project reports.
* **Statistics**: Display project statistics.

## Tools Menu

* **Interface Scale**: Adjust interface scaling.
* **Install Plugins**: Access plugins for Houdini and Unreal Engine.
* **Run Diagnostics**: Execute system and application checks.
* **Console**: Open console for debugging.
* Verbose Logging: Enables detailed logging for enhanced troubleshooting and analysis.
* **Options**: Access application settings.

## Help Menu

* **User Guide**: Open the Gaea user manual.
* **Node Reference**: Reference guide for nodes.
* **Shortcut Reference**: List of keyboard shortcuts.
* **What's New**: View recent updates in the software.
* **Check for Updates**: Manually check for updates.
* **Manage License**: Access license management options.
* **Diagnostics**: Open diagnostics tools.
* **About Gaea**: Display version and credits for Gaea.
