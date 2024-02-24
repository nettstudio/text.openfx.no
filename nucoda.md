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
``markup`` | **Markup** | Parse text as markup
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

# Limitations

Nucoda has limited support for OpenFX string parameters. This limits the usability of the text input user interface. As a workaround use the text file option in TextOFX (edit text in notepad or similar).

If you want proper text input contact [Filmworkz](https://filmworkz.com/nucoda/) and request support for `kOfxParamStringIsMultiLine` in Nucoda.

# Fonts

Nucoda will scan for new fonts on each launch.

Search locations:

1. `C:\Windows\Fonts`
2. `C:\Users\USERNAME\AppData\Local\Microsoft\Windows\Fonts`
3. `C:\Users\USERNAME\.fonts`

The font cache is stored in `C:\Users\USERNAME\AppData\Local\fontconfig\cache`.

TrueType fonts (TTF) are recommended.

# Markup

TextOFX allows you to format text further using a simple markup language. This means you can easily make certain parts of your text bold, italic, smaller, bigger, or even change the font.

## Examples

#### Simple Lower Thirds

Text input *(remember to enable ``markup`` parameter)*:

```
<span font="Futura Bold 50">John Doe</span>
<span font="Futura Italic 25">Work title, at Company</span>
```

Result:

![Lower Thirds output](assets/images/textofx-markup-example-01.png)

## Attributes/Tags
The most general markup tag is **``<span>``**, then there are some convenience tags:

* **``<b>``** - Bold
* **``<i>``** - Italic
* **``<s>``** - Strikethrough
* **``<u>``** - Underline

**``<span>``**

* **``font=""``**
  * A font description string, such as “Sans Italic 12”. Note that any other span attributes will override this description. So if you have “Sans Italic” and also a ``style=”normal”`` attribute, you will get Sans normal, not italic.

* **``size=""``**
  * Font size in 1024ths of a point, or in points (e.g. ‘12.5pt’), or one of the absolute sizes ‘xx-small’, ‘x-small’, ‘small’, ‘medium’, ‘large’, ‘x-large’, ‘xx-large’, or a percentage (e.g. ‘200%’), or one of the relative sizes ‘smaller’ or ‘larger’.
* **``style=""``**
  * One of ‘normal’, ‘oblique’, ‘italic’.
* **``weight=""``**
  * One of ‘ultralight’, ‘light’, ‘normal’, ‘bold’, ‘ultrabold, ‘heavy’, or a numeric weight.
* **``variant=""``**
  * One of ‘normal’, ‘small-caps’, ‘all-small-caps’, ‘petite-caps’, ‘all-petite-caps’, ‘unicase’, ‘title-caps’.
* **``stretch=""``**
  * One of ‘ultracondensed’, ‘extracondensed’, ‘condensed’, ‘semicondensed’, ‘normal’, ‘semiexpanded’, ‘expanded’, ‘extraexpanded’, ‘ultraexpanded’.
* **``underline=""``**
  * One of ‘none’, ‘single’, ‘double’, ‘low’, ‘error’.
* **``overline=""``**
  * One of ‘none’ or ‘single’.
* **``strikethrough=""``**
  * ‘true’ or ‘false’ whether to strike through the text.
* **``letter_spacing=""``**
  * Inter-letter spacing in 1024ths of a point.
* **``allow_breaks=""``**
  * ‘true’ or ‘false’ to indicate whether breaking lines is allowed.
* **``line_height=""``**
  * Overrides the line height. The value can be either a factor (< 1024) that is used to scale up the logical extents of runs or an absolute value (in 1024th of a point).
* **``text_transform=""``**
  * Specifies how characters are transformed during shaping. The values can be ‘none’, ‘lowercase’, ‘uppercase’ or ‘capitalize’.

# Support

For support inquiries use **support at openfx dot no**.
