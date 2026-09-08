# animatica-assets-public

3D assets to download - [animatica.ai](https://animatica.ai).

Every asset ships geometry, a shading network and (where one exists) a rig
in native application formats, plus universal USD/FBX sources with textures.

For a rigged asset the source FBX is not geometry alone: it carries the
skeleton and the skin in rest pose, with embedded textures and no animation.
The animations stay in the native scenes.

## Downloading

The repo uses Git LFS - install it before cloning:

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

| Asset | Version | Applications | License |
|---|---|---|---|
| [Animatica Hero](assets/animatica-hero/) | v003 | Blender, Maya, 3ds Max, Unreal Engine | owned by Animatica · Animatica |
| [Blocky Character](assets/blocky-character/) | v002 | Blender, Maya, 3ds Max, Unreal Engine | CC0 1.0 (public domain) · Kenney |
| [Cesium Man](assets/cesium-man/) | v002 | Blender, Maya, 3ds Max, Unreal Engine | CC BY 4.0 · Cesium |
| [Test Cube](assets/test-cube/) | v005 | Blender, Maya, 3ds Max, Unreal Engine | owned by Animatica · Animatica |

Machine-readable listing: [index.json](index.json).

