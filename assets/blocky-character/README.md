# Blocky Character

Version **v001** (2026-08-21). Units: meters.

import of Blocky Character (Kenney, CC0)

![preview](preview/thumbnail.png)

## Contents

| Application | Folder | Rig |
|---|---|---|
| universal | source/ (USD with shading + FBX + textures) | - |
| Blender | blender/ | yes |
| Maya | maya/ | no |
| 3ds Max | max/ | no |
| Unreal Engine 5.8.1 | unreal/ | no |

## Opening the files

Unpack the Releases zip whole - texture paths are relative and assume that
`source/` sits next to the application folders.

- **Blender** - open the file in `blender/`. Textures are linked by relative
  paths, so they work straight away. Do not move the `source/` folder.
- **Maya** - set the project first (File > Set Project) to the `maya/` folder,
  and only then open the scene. Textures resolve through the project.
- **3ds Max** - set the project first (File > Project > Set Active Project)
  to the `max/` folder, and only then open the scene.
- **Unreal Engine** - copy the contents of `unreal/Content/` into your
  project's `Content/` folder. The `.uasset` files are versioned: they open
  in the engine version listed in the table above or newer, but not older.
  If you need an older version, import `source/` yourself.
- **Houdini, Omniverse and the rest** - open `source/<asset>.usd`. The USD
  already carries its shading (`UsdPreviewSurface` + textures, relative
  paths), so nothing needs wiring by hand. Copy the whole `source/` folder.

Textures follow the PBR Metallic-Roughness convention. The `Normal` channel
is OpenGL normals (Blender, Maya, Houdini), `NormalDX` is DirectX (3ds Max,
Unreal).

A note for Maya: its USD importer ignores `sourceColorSpace` and assigns sRGB
to every texture. In Maya, use the prepared scene in `maya/` - it has the
correct color space.

## License

**CC0 1.0 (public domain)** - https://kenney.nl/assets/blocky-characters

Author / rights holder: **Kenney**.

