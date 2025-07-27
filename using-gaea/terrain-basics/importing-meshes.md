---
icon: '7'
---

# Importing Meshes

Gaea 2.1 introduces the Object node which can be used to import 3D models and rasterize them into heightfields. You can fully control the Scale, Rotation, and Movement of the imported mesh. The only limitation is that the 3D mesh is projected and rasterized into a 2.5D heightfield.

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

Once imported, the model will behave exactly like any other Gaea generated terrain, and you can do anything with it.&#x20;

<figure><img src="../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

The Object node requires the original mesh to be present during build. If you are not going to have access to the mesh later, you may wish to [Bake the Object node](../baking-nodes/).

{% hint style="info" %}
Please note that Gaea is a heightfield-first software. While we do our best to support as many kinds of meshes and objects, sometimes very large or very complex objects may not import that well. You may wish to use applications such as MeshLabs to simplify or recontainerize your mesh
{% endhint %}

