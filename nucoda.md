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

# Support

For support inquiries use **support at openfx dot no**.
