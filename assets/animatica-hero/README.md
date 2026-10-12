# Animatica Hero

Version **v004** (2026-09-30). Units: meters.

rig.json + control layers per DCC (Rigify / HIK / IK Rig / Max controls script), MotionBuilder variant, stamps in the source FBX

![preview](preview/thumbnail.png)

## Contents

| Application | Folder | Rig | Controls |
|---|---|---|---|
| universal | source/ (USD with shading + FBX + textures) | yes (77 bones) | - |
| Blender | blender/ | yes | rigify |
| Maya | maya/ | yes | animatica |
| MotionBuilder | mobu/ | yes | hik-definition |
| 3ds Max | max/ | yes | script |
| Unreal Engine 5.8.1 | unreal/ | yes | ikrig |

## Opening

Unpack the Releases zip whole - texture paths are relative and assume that
`source/` sits next to the application folders.

The source FBX carries the skeleton and the skin in rest pose with embedded
textures and no animation. Its root joint carries the `animatica_*` custom
properties the Animatica MotionBuilder plugin reads, so a canonical rig is
listed without Adopt; `mobu/` holds the FBX with the HumanIK definition. The
MotionBuilder viewport shows the model grey until you switch Renderer to
USD Renderer - the textures are embedded in the file either way.

- **Blender** - append the collection `animatica-hero` from `blender/animatica-hero.blend`
  (File > Append > Collection). Textures are linked by relative paths
  to `source/textures/` - do not move the `source/` folder.
- **Maya** - set the project to the `maya/` folder (File > Set Project),
  then import `maya/animatica-hero.ma`. Textures resolve through the project.
- **MotionBuilder** - open `mobu/animatica-hero.fbx` (File > Open).
- **3ds Max** - merge `max/animatica-hero.max` and set the project to the `max/`
  folder (File > Project > Set Active Project). For the control layer run
  `max/animatica-hero_controls.ms` (Scripting > Run Script).
- **Unreal Engine** - copy the contents of `unreal/Content/` into your
  project's `Content/` folder. The `.uasset` files are versioned: they open
  in the engine version listed in the asset's Contents table or newer, but
  not older. If you need an older version, import `source/` yourself.
- **Houdini, Omniverse and the rest** - open `source/animatica-hero.usd`. The USD
  already carries its shading (`UsdPreviewSurface` + textures, relative
  paths), so nothing needs wiring by hand. Copy the whole `source/` folder.

Textures follow the PBR Metallic-Roughness convention. The `Normal` channel
is OpenGL normals (Blender, Maya, Houdini), `NormalDX` is DirectX (3ds Max,
Unreal).

A note for Maya: its USD importer ignores `sourceColorSpace` and assigns sRGB
to every texture. In Maya, use the prepared scene in `maya/` - it has the
correct color space.

## License

**owned by Animatica**

Author / rights holder: **Animatica**.

