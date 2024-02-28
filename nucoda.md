---
title: "OpenFX Text Integration for Filmworkz Nucoda and Phoenix"
description: "Elevate your projects with full-fledged text creation and animation seamlessly integrated within your existing Nucoda/Phoenix workflow, powered by our advanced OpenFX text generator."
layout: nucoda
permalink: nucoda.html
latest_version: "v1.1.1-37c6551"
demo_sha256: "142498d9039b6c6a80e4e3f7204cfe116dc0efcae5554cfa30777e3dc52aa3d3"
rel_sha256: "fc24e24691adb487e4bad4705aee81a7fe0a6eb0d078414c82e10b56a95580f8"
rel_branch: "v1.1-nucoda"
rel_prefix: "TextOFX-Nucoda"
rel_suffix: "Windows-x64.zip"
gumroad: "https://rodlie.gumroad.com/l/textofx-v1-1-nucoda"
---

# Changes

* ``v1.1.1-37c6551``
  * Added support for Filmworkz Phoenix 2024.1
* ``v1.1.0-81c433a``
  * Initial release for Filmworkz Nucoda 2024.1

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

1. Close Nucoda/Phoenix before proceeding.
2. Open the extracted folder and double-click on `Setup.exe`.
3. Follow the on-screen instructions to complete the installation.
4. Launch Nucoda/Phoenix. TextOFX will be available as an effect under `Text/Text Generator`.

**Manual Installation**

1. Close Nucoda/Phoenix before proceeding.
2. Copy `TextNucoda.ofx.bundle` from the extracted folder into `C:\Program Files\Common Files\OFX\Plugins\`.
3. Launch Nucoda/Phoenix. TextOFX should now be available as an effect under `Text/Text Generator`.

# Fonts

Nucoda/Phoenix will scan for new fonts on each launch.

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
