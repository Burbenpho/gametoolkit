# Ludusavi - Backup Your Game Saves

Ludusavi is a cross-platform tool for backing up your PC video game save data.  It supports a wide range of game stores, including Steam, Epic Games Store, GOG, and more.

This is simple custom manifest for my own usage.


## Table of Contents
- [Installation](#installation)
- [Manifest Guide](#manifest-guide)
- [Creating Custom Manifests](#creating-custom-manifests)
- [List of supported games](#list-of-supported-games)
- [Credits](#credits)
  


## Installation

You can download the latest release of Ludusavi from the [Ludusavi releases page](https://github.com/mtkennerly/ludusavi/releases).

In OTHER tab add [link](https://raw.githubusercontent.com/Burbenpho/ludusavi-manifest/refs/heads/main/manifest.yaml) to manifests list.

**WARNING:** Steam, GOG, EGS saving is not guaranteed.
## Manifest Guide

Ludusavi uses a YAML-based manifest file to define the save locations for each game. This allows for flexible and accurate backups.  The primary manifest is available at [Ludusavi Manifest](https://github.com/mtkennerly/ludusavi-manifest). This guide details the structure and usage of the manifest files.

## Creating Custom Manifests

Because the default manifest may not cover all games or platforms, creating custom manifests is crucial for comprehensive backups.  The structure of a manifest file is as follows:

#### Simple only folder example
```yaml project="ludusavi-manifest" file="example_manifest.yaml" version=1
My Game: # whitespaces allowed
  files:
    "C:/Any/Folder/Path": # see more in ludusavi-manifest guide
      tags:
        - save
```
Remember to replace placeholders like `"My Game"` your actual game names and save locations.  You can add multiple paths per game to cover different save locations.

## Placholders
*This information was taken from the [Ludusavi Manifest Format documentation.](https://github.com/mtkennerly/ludusavi-manifest#Format)*

| placeholder            | meaning                                                                                |
|------------------------|----------------------------------------------------------------------------------------|
| `<root>`               | a directory where games are installed (configured in backup tool)                      |
| `<game>`               | an `installDir` (if defined) or the game's canonical name in the manifest              |
| `<base>`               | shorthand for `<root>/<game>` (unless overridden by store-specific rules)              |
| `<home>`               | current user's home directory in the OS (`~`)                                          |
| `<storeGameId>`        | a store-specific `id` from the manifest, corresponding to the root's store type        |
| `<storeUserId>`        | current user's ID in the game store                                                    |
| `<osUserName>`         | current user's name in the OS                                                          |
| `<winAppData>`         | `%APPDATA%` on Windows                                                                 |
| `<winLocalAppData>`    | `%LOCALAPPDATA%` on Windows                                                            |
| `<winLocalAppDataLow>` | `<home>/AppData/LocalLow` on Windows                                                   |
| `<winDocuments>`       | `<home>/Documents` (f.k.a. `<home>/My Documents`) or a localized equivalent on Windows |
| `<winPublic>`          | `%PUBLIC%` on Windows                                                                  |
| `<winProgramData>`     | `%PROGRAMDATA%` on Windows                                                             |
| `<winDir>`             | `%WINDIR%` on Windows                                                                  |
| `<xdgData>`            | `$XDG_DATA_HOME` on Linux                                                              |
| `<xdgConfig>`          | `$XDG_CONFIG_HOME` on Linux                                                            |
## List of supported games
- Tyrant's Realm (Windows)
- Lorn's Lure (Windows, Linux, macOs)

...more will be added in future!
## Credits 

[Ludusavi](https://github.com/mtkennerly/ludusavi) was created by [mtkennerly](https://github.com/mtkennerly) and is licensed under the MIT License. 
