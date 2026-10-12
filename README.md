# animatica-assets-public

3D assets to download - [animatica.ai](https://animatica.ai).

Every asset ships geometry, a shading network and (where one exists) a rig
in native application formats, plus universal USD/FBX sources with textures.

For a rigged asset the source FBX is not geometry alone: it carries the
skeleton and the skin in rest pose, with embedded textures and no animation.
No animation is shipped; the native scenes carry the control layers.

## Downloading

Simplest: **download a single asset's zip** from the table below or from
the [Releases](https://github.com/animatica-ai/animatica-assets-public/releases) tab.
Neither git nor Git LFS is needed for that.

Alternatively the whole repo (requires Git LFS):

```bash
git lfs install
git clone https://github.com/animatica-ai/animatica-assets-public.git
```

A single asset through git, without pulling everything:

```bash
git clone --filter=blob:none --no-checkout https://github.com/animatica-ai/animatica-assets-public.git
cd animatica-assets-public
git sparse-checkout set assets/ASSET-NAME
git checkout
```

## Assets

| Asset | Version | Applications | Controls | License | Zip |
|---|---|---|---|---|---|
| [Animatica Hero](assets/animatica-hero/) | v004 | Blender, Maya, MotionBuilder, 3ds Max, Unreal Engine | Blender: rigify, Maya: animatica, MotionBuilder: hik-definition, 3ds Max: script, Unreal Engine: ikrig | owned by Animatica · Animatica | [download](https://github.com/animatica-ai/animatica-assets-public/releases/download/animatica-hero-v004/animatica-hero-v004.zip) |
| [Cesium Man](assets/cesium-man/) | v003 | Blender, Maya, MotionBuilder, 3ds Max, Unreal Engine | Blender: rigify, Maya: animatica, MotionBuilder: -, 3ds Max: script, Unreal Engine: ikrig | CC BY 4.0 · Cesium | [download](https://github.com/animatica-ai/animatica-assets-public/releases/download/cesium-man-v003/cesium-man-v003.zip) |

## Opening

Each asset's README carries the same recipe with its own file names.

- **Blender** - append the collection `ASSET-NAME` from `blender/ASSET-NAME.blend`
  (File > Append > Collection). Textures are linked by relative paths
  to `source/textures/` - do not move the `source/` folder.
- **Maya** - set the project to the `maya/` folder (File > Set Project),
  then import `maya/ASSET-NAME.ma`. Textures resolve through the project.
- **3ds Max** - merge `max/ASSET-NAME.max` and set the project to the `max/`
  folder (File > Project > Set Active Project). Where
  `max/ASSET-NAME_controls.ms` ships, run it (Scripting > Run Script)
  for the control layer.
- **MotionBuilder** - open `mobu/ASSET-NAME.fbx` (File > Open).
- **Unreal Engine** - copy the contents of `unreal/Content/` into your
  project's `Content/` folder. The `.uasset` files are versioned: they open
  in the engine version listed in the asset's Contents table or newer, but
  not older. If you need an older version, import `source/` yourself.
- **Houdini, Omniverse and the rest** - open `source/ASSET-NAME.usd`. The USD
  already carries its shading (`UsdPreviewSurface` + textures, relative
  paths), so nothing needs wiring by hand. Copy the whole `source/` folder.

Machine-readable listing: [index.json](index.json).

