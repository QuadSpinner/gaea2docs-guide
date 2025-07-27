# File Formats

Gaea supports all modern (and some legacy) file formats for both flat files and meshes.

## For Import

### **Bitmap Formats**

<table><thead><tr><th width="280">Format</th><th data-type="checkbox">32-bit</th><th data-type="checkbox">16-bit</th><th data-type="checkbox">8-bit</th></tr></thead><tbody><tr><td>OpenEXR</td><td>true</td><td>false</td><td>false</td></tr><tr><td>TIFF</td><td>true</td><td>true</td><td>true</td></tr><tr><td>PNG (64 / 16 / 8)</td><td>true</td><td>true</td><td>true</td></tr><tr><td>RAW (Float / Half / UShort)</td><td>true</td><td>true</td><td>false</td></tr><tr><td>JPG</td><td>false</td><td>false</td><td>false</td></tr><tr><td>Gaea RAW</td><td>true</td><td>false</td><td>false</td></tr></tbody></table>

{% hint style="info" %}
Raw can be saved as .raw, .r16, and .r32 as required as different applications use different combinations of format and extensions.
{% endhint %}

### 3D Formats

* Wavefront OBJ (.obj)
* Autodesk Filmbox (.fbx)
* Collada (.dae)
* WebGL (.glTF/.glb)
* Point Cloud (.xyz)

## **For Import**

Gaea supports the following formats for importing data:

* .exr
* .tif/.tiff
* .webp/.jpeg
* .webp
* .svg
* .psd
* .hdr
* .pfm
* .r32
* .raw
* .bmp

{% hint style="info" %}
Gaea can also import 3D objects with the Object node.
{% endhint %}



## Gaea's Project Formats <a href="#gaea-27s-project-formats" id="gaea-27s-project-formats"></a>

Gaea saves files in the formats mentioned below.

### **.terrain**

Gaea terrain projects are saved as a `.terrain` file. All Gaea editions can read this format.

See [#advanced-automation](../automation/command-line-automation.md#advanced-automation "mention") for manipulating this file format.



## Precision <a href="#precision" id="precision"></a>

Gaea stores and processes its heightfields in 32-bit floating points, which is compatible with all professional CGI applications.

### **32-bit**

For practical purposes, exporting as either OpenEXR or TIFF will give you the best results and maximum compatibility with other applications. If you are using a custom pipeline, using R32 or PFM formats may be of more use. See the section below for those formats.

{% hint style="info" %}
If you are saving output from Gaea to bring back to Gaea either in the same or different file, we recommend using the `.r32` or `.graw` formats for maximum fidelity and efficiency.
{% endhint %}

### **16-bit**

While displacement/heightfield information requires 32-bit precision for accuracy; color maps, masks, and other secondary data which may have fewer levels of complexity can make use of 16-bit formats, such as PNG. This can help save on disk space as larger worlds will require a lot of storage space. Storing in 16-bit also helps performance.

In fact, if your terrain does not contain many smooth details, you can even export your main displacement as 16-bit.

Game engines, such as Unity, can only import RAW 16-bit (ushort) format terrains.

### **8-bit**

In some cases, for example with black and white masks, you may not need a high level of precision at all. You can use 8-bit PNG or TIFF output which can increase performance and save disk space.

**Custom Workflows Precision**

If you are using Gaea in a custom workflow, such as automation, you may require the data to be as simple and efficiently readable as possible.

### Technical Details

32-bit float (.r32) and 16-bit ushort (.raw) are the simplest formats you can use. It is a simple binary array of `float` (IEEE 754) or `unsigned short`. The file has no header and can be read directly as a binary stream. The files will use Little Endian.

The size of the heightfield should be square root of the byte length divided by the size of the type (4 bytes for `float`, 2 bytes for `ushort`).

The `.r32` format will store values between `0.0f` and `1.0f`. While the `.raw` format will store values between `0` and `65535`.

Both formats are recommended for heightfield (grayscale) data only.
