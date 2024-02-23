---
title: "OpenFX Text Integration for Filmworkz Nucoda"
description: "Elevate your projects with full-fledged text creation and animation seamlessly integrated within your existing Nucoda workflow, powered by our advanced OpenFX text generator."
layout: nucoda
permalink: nucoda.html
image: assets/images/Nucoda_with_Precision_Panel_and_Dolby_Reference_Monitor.jpg
latest_version: "v1.1.0-81c433a"
demo_sha256: "3c53edd9430c1714f72065bd5573793313b90ea6af9d1823b8c854f75aa9179e"
rel_sha256: "06c99fe8651cfda8c844743ed0ddf4434a1f34a6722d34069c4815cbad022d2f"
rel_branch: "v1.1-nucoda"
rel_prefix: "TextOFX-Nucoda"
rel_suffix: "Windows-x64.zip"
gumroad: "https://rodlie.gumroad.com/l/textofx-v1-1-nucoda"
---

# Parameters

ID | Label | Description
--- | --- | ---
``size`` | **Size** | Font size in pixels.
``strokeSize`` | **Stroke** | Stroke size.
``letterSpace`` | **Letter spacing** | Spacing between letters.
``lineSpace`` | **Line spacing** | Spacing between lines.
``color`` | **Fill** | The text fill color.
``strokeColor`` | **Stroke** | The stroke fill color.
``wrap`` | **Word wrap** | Wrap the lines to the desired width.
``halign`` | **Horizontal align** | Horizontal text align.
``valign`` | **Vertical align** | Vertical text align.
``style`` | **Style** | Font family style.
``weight`` | **Weight** | The weight field specifies how bold or light the font should be.
``stretch`` | **Stretch** | Width of the font relative to other designs within a family.
``translate`` | **Translate** | Enable translate.
``position`` | **Position** | Custom position of the text layout, if translate is enabled.
``layoutWidth`` | **Custom Width** | Set width for the text layout when using translate (custom position). Default (0) is the width of the text or source/project format.
``scale`` | **Scale** | Scale the text layout.
``skewX`` | **Skew X** | Skew the text layout *(X)*.
``skewY`` | **Skew Y** | Skew the text layout *(Y)*.
``rotate`` | **Rotate** | Rotate the text layout.
``name`` | **Select font** | Select the font family to be used.
``font`` | **Font** | Font family in use.
``text`` | **Text** | The text that will be drawn.
``markup`` | **Markup** | Parse text as [Pango Text Attribute Markup Language](https://docs.gtk.org/Pango/pango_markup.html).
``file`` | **File** | Import text or markup from file.
``reloadText`` | **Reload Text File** | Reload Text File.

# Installation

Extract the contents of the `TextOFX-Nucoda-VERSION-Windows-x64.zip` file to a temporary location.

**Automatic Installation**

1. Close Nucoda before proceeding.
2. Open the extracted folder and double-click on `Setup.exe`.
3. Follow the on-screen instructions to complete the installation.
4. Launch Nucoda. TextOFX will be available as an effect under `Text/Text Generator`.

**Manual Installation**

1. Close Nucoda before proceeding.
2. Copy `TextOFXNucoda.ofx.bundle` from the extracted folder into `C:\Program Files\Common Files\OFX\Plugins\`.
3. Launch Nucoda. TextOFX should now be available as an effect under `Text/Text Generator`.

# Fonts

Nucoda will scan for new fonts on each launch.

Search locations:

1. `C:\Windows\Fonts`
2. `C:\Users\USERNAME\AppData\Local\Microsoft\Windows\Fonts`
3. `C:\Users\USERNAME\.fonts`

The font cache is stored in `C:\Users\USERNAME\AppData\Local\fontconfig\cache`.

TrueType fonts (TTF) are recommended.

# Limitations

Nucoda has limited support for OpenFX string parameters. This limits the usability of the text input user interface. As a workaround use the text file option in TextOFX (edit text in notepad or similar).

If you want proper text input contact [Filmworkz](https://filmworkz.com/nucoda/) and request support for `kOfxParamStringIsMultiLine` in Nucoda.

# Support

For support inquiries use **support at openfx dot no**.
