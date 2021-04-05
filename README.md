The Zitga Unity Style Guide
===========================

### For file structure, naming conventions and other things

These are guidelines for keeping your project organized and allow your team to quickly find the assets they need. Games are large projects that span several months, thus having standardized conventions that make sense will avoid headaches in the long run.

Note that your team and project might have different needs, use different software, etc. Use this guide only as a base to decide on what works for your team. Every project should have its own, easy to find, style guide, so everyone in the team is up to date in the project's conventions.

# Table of Contents

- [Asset Naming](#asset-naming)
    - [Folders](#folders)
    - [Source code](#source-code)
    - [Non-code assets](#non-code-assets)
- [Directory/File structure](#directory-file-structure)
    - [Assets](#assets)
    - [Scripts](#scripts)
- [Workflow](#workflow)
    - [Localization](#localization)
    - [Audio](#audio)
- [Be Consistent](#be-consistent)

# Asset Naming

First of all, no `spaces` on file or directory names.

## Folders

`PascalCase`

Prefer a deep folder structure over having long asset names.

Directory names should be as concise as possible, prefer one or two words. If a directory name is too long, it probably makes sense to split it into sub directories.

## Source Code

Use the naming convention of the programming language. For C# and shader files use `PascalCase`, as per C# convention.

## Non-Code Assets

Use `tree_small` not `small_tree`. While the latter sound better in English, it is much more effective to group all tree objects together instead of all small objects.

Prefer using descriptive suffixes instead of iterative: `vehicle_truck_damaged` not `vehicle_truck_01`. If using numbers as a suffix, always use 2 digits. And **do not** use it as a versioning system! Use `git` or something similar.

### Persistent/Important GameObjects

`_snake_case`

Use a leading underscore to make object instances that are not specific to the current scene stand out.

# Directory/File Structure

```
Root
+---Assets
+---Build
\---Tools           # Programs to aid development: compilers, asset managers etc.
```

## Assets

```
Assets
+---ProjectName
|   +---Art
|   |   +---Materials
|   |   +---Models      # FBX and BLEND files
|   |   +---Music
|   |   +---Prefabs
|   |   +---Sound       # Samples and sound effects
|   |   +---Textures
|   |   +---UI
|   |   +---Shaders
|   +---CSV             # Csv files
|   +---Scenes          # Unity scene files
|   +---Scripts
+---ThirdParties
|   +---PluginX
|   +---PluginY
```

# Workflow

## Localization

File extension: `CSV`

Widely used by localization software, makes it trivial to edit strings using spreadsheets.

## Audio

File extension: `WAV` while mixing, `OGG` in game.

Preload small sound clips to memory, load on the fly for longer music and less frequent ambient noise files.

# Be Consistent

> The point of having style guidelines is to have a common vocabulary of coding so people can concentrate on what you're saying rather than on how you're saying it. We present global style rules here so people know the vocabulary, but local style is also important. If code you add to a file looks drastically different from the existing code around it, it throws readers out of their rhythm when they go to read it. Avoid this.

-- [Unity Style Guide](https://github.com/stillwwater/UnityStyleGuide)

---
