---
name: differential-upload
description: Understand differential upload UX.
---
# Differential Upload Guide

## What is Differential Upload?

Differential Upload is a smarter, faster way to get your work onto the Render Network. Instead of packaging your entire scene into a single large file (like a `.zip` archive) every time you want to render, you simply upload your **working project folder**.

### Why is it called "Differential"?
The name comes from the fact that the Render Network calculates the *difference* between what is on your computer and what is already on the Render Network. It uploads **only** the files that are new or have changed.

### How does it work?
The Render Network remembers every asset (textures, VDBs, meshes etc) you have ever uploaded in the past. When you upload a project folder:
1.  The app scans your folder and identifies every file.
2.  It checks with the Network to see if any of these files exist there from *any* of your previous jobs.
3.  If a file (like a heavy 4GB texture) was uploaded months ago for a different project, the app skips uploading it again. Render Network instantly links the existing copy to your new job.
4.  Only truly new files are uploaded.
5.  Main scene file is **always** uploaded.

## Advantages

**Speed & Efficiency**:\
If you change just one texture or move a camera in your scene, you don't need to re-upload the whole project. The app recognizes files you've already uploaded and skips them.

**No Repacking**:\
Save time by skipping the export/zipping step. Just work in your folder and upload the folder.

## How to use it

### 1. Preparing Your Project Folder

You can organize your folders however you like. Nested folders, deep hierarchies, and linked assets are fully supported. There is just **one important rule**:

> Your project folder must have **exactly one** main scene file (e.g., `.c4d`, `.blend`, `.ocs`) in the **top-level (root)** of the folder.

### 2. Uploading

Simply drag and drop your project folder into the Render Network Manager. The app will handle the rest.

## Project Folder Structure

*   **Allowed**: Any number of subfolders, textures, and assets. You can even have other scene files inside subfolders (they will be treated as regular assets).
*   **Not Allowed**: Two different versions of your scene file (e.g., `scene_v1.blend` and `scene_v2.blend`) sitting together in the main folder root.

### Example of Correct Structure (Simple)

```text
my-project/
├── test_shot.c4d  <-- ✅ The ONE main scene file
├── texture_A.png  <-- ✅ Assets can sit next to the scene
└── texture_B.jpg
```

### Example of Correct Structure (Complex)

```text
my-project/
├── main_scene_v05.c4d  <-- ✅ The ONE main scene file
├── textures/
│   ├── ground/
│   │   ├── diffuse.jpg
│   │   └── normal.png
│   └── walls/
│       └── wall_base.png
├── other-assets/
│   ├── meshes/
│   │   └── spaceship_model.obj
│   └── linked-scenes/
│       └── background_city.c4d  <-- ✅ Linked .c4d in a subfolder is fine
└── vdb/
    └── smoke_cache.0001.vdb
    └── smoke_cache.0002.vdb
    └── smoke_cache.0003.vdb
```

### Example of Incorrect Structure
The app won't know which file is the main scene.

```text
my-project/
├── shot_01.blend  <-- ❌ Conflict
├── shot_02.blend  <-- ❌ Conflict (Too many scene files in root)
├── textures/
└── ...
```

To fix this, simply move `shot_02.blend` into a subfolder (e.g., `backup/`) or remove it from the folder before uploading.

