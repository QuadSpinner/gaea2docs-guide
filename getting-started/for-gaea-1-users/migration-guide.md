# Migration Guide

Gaea 2.0 was rewritten from the ground up. Many nodes, settings, and paradigms have changed. This page covers some of the major changes and replacements.This page is under construction. Please check back later.

## File Compatibility <a href="#file-compatibility" id="file-compatibility"></a>

Gaea 1.0 `.tor` files are _not_ compatible with Gaea 2.0 `.terrain` files as the engines are completely different.

You should use Gaea 1.0 for older projects. If you need to bring in terrain from Gaea 1.0 into 2.0, the most precise and direct way is to save the output as R32 from Gaea 1.0 and import it into 2.0.

If you used fixed filenames, you can refresh the input in Gaea 2.0 whenever you rebuild the output in Gaea 1.0.

## Nodes <a href="#nodes" id="nodes"></a>

Many of the GeoPrimitives and all of the LookDev nodes have been retired. These have been replaced with the new Landscape and Surface nodes.​​​ Some nodes have been renamed for clarity.

See [node-changes.md](node-changes.md "mention") for a detailed list of changes.

### ​ <a href="#undefined" id="undefined"></a>
