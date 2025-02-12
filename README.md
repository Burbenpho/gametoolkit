# Ludusavi - Backup Your Game Saves

Ludusavi is a cross-platform tool for backing up your PC video game save data.  It supports a wide range of game stores, including Steam, Epic Games Store, GOG, and more.

This is simple custom manifest for my own usage.

**Important Considerations:**  Currently, the default manifest may not fully support backing up games outside the standard Windows AppData folder or Linux applications.  Custom manifests are required for comprehensive support in these cases. [1](https://github.com/mtkennerly/ludusavi)

## Table of Contents
- [Installation](#installation)
- [Manifest Guide](#manifest-guide)
- [Creating Custom Manifests](#creating-custom-manifests)
- [List of supported saves](#lists)
- [Credits](#credits)
  


## Installation

You can download the latest release of Ludusavi from the [GitHub Releases page](https://github.com/mtkennerly/ludusavi/releases). [1](https://github.com/mtkennerly/ludusavi)


## Manifest Guide

Ludusavi uses a YAML-based manifest file to define the save locations for each game. This allows for flexible and accurate backups.  The primary manifest is available at [Ludusavi Manifest](https://github.com/mtkennerly/ludusavi-manifest). [1](https://github.com/mtkennerly/ludusavi)  This guide details the structure and usage of the manifest files.

## Creating Custom Manifests

Because the default manifest may not cover all games or platforms, creating custom manifests is crucial for comprehensive backups.  The structure of a manifest file is as follows:
### Simple only folder example
```yaml project="ludusavi-manifest" file="example_manifest.yaml" version=1
My Game: # whitespaces allowed
  files:
    "C:/Any/Folder/Path": # see more in ludosavi-manifest guide
      tags:
        - save
```

Remember to replace placeholders like `"My Game"` your actual game names and save locations.  You can add multiple paths per game to cover different save locations.


## Contributing

Contributions to Ludusavi are welcome! Please see the [CONTRIBUTING.md](https://github.com/mtkennerly/ludusavi/blob/main/CONTRIBUTING.md) file for details. [1](https://github.com/mtkennerly/ludusavi)


## Credits

Ludusavi was created by [mtkennerly](https://github.com/mtkennerly) and is licensed under the MIT License. [1](https://github.com/mtkennerly/ludusavi)
