# Cesium Man

Version **v002** (2026-09-08). Units: meters.

rigged source: skeleton and skin in rest pose, embedded textures; animation stays in the Blender variant

![preview](preview/thumbnail.png)

## Contents

| Application | Folder | Rig |
|---|---|---|
| universal | source/ (USD with shading + FBX + textures) | yes (19 bones) |
| Blender | blender/ | yes |
| Maya | maya/ | yes |
| 3ds Max | max/ | yes |
| Unreal Engine 5.8.1 | unreal/ | yes |

## Opening the files

Unpack the Releases zip whole - texture paths are relative and assume that
`source/` sits next to the application folders.

The source FBX carries the skeleton and the skin in rest pose with embedded
textures and no animation - the animations live in the Blender variant. In
MotionBuilder untick "canonical skeletons only" and use Adopt: the FBX does
not carry the `animatica_*` custom properties yet.

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

**CC BY 4.0** - https://github.com/KhronosGroup/glTF-Sample-Assets/tree/main/Models/CesiumMan

Author / rights holder: **Cesium**.
This license requires crediting the author on further use.

