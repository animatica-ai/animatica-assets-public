# animatica-assets-public

Assety 3D do pobrania - [animatica.ai](https://animatica.ai).

Kazdy asset zawiera geometrie, shading network i (jesli istnieje) rig
w natywnych formatach aplikacji oraz uniwersalne zrodla USD/FBX z teksturami.

## Pobieranie

Najprosciej: **pobierz zip pojedynczego assetu** z tabeli nizej albo
z zakladki [Releases](https://github.com/animatica-ai/animatica-assets-public/releases).
Nie trzeba do tego gita ani Git LFS.

Alternatywnie cale repo (wymaga Git LFS):

```bash
git lfs install
git clone https://github.com/animatica-ai/animatica-assets-public.git
```

Pojedynczy asset przez gita, bez sciagania calosci:

```bash
git clone --filter=blob:none --no-checkout https://github.com/animatica-ai/animatica-assets-public.git
cd animatica-assets-public
git sparse-checkout set assets/NAZWA-ASSETU
git checkout
```

## Assety

| Asset | Wersja | Aplikacje | Licencja | Zip |
|---|---|---|---|---|
| [Blocky Character](assets/blocky-character/) | v001 | Blender, Maya, 3ds Max, Unreal Engine | CC0 1.0 (domena publiczna) · Kenney | [pobierz](https://github.com/animatica-ai/animatica-assets-public/releases/download/blocky-character-v001/blocky-character-v001.zip) |
| [Cesium Man](assets/cesium-man/) | v001 | Blender, Maya, 3ds Max, Unreal Engine | CC BY 4.0 · Cesium | [pobierz](https://github.com/animatica-ai/animatica-assets-public/releases/download/cesium-man-v001/cesium-man-v001.zip) |
| [Test Cube](assets/test-cube/) | v004 | Blender, Maya, 3ds Max, Unreal Engine | wlasnosc Animatica · Animatica | [pobierz](https://github.com/animatica-ai/animatica-assets-public/releases/download/test-cube-v004/test-cube-v004.zip) |

Lista maszynowa: [index.json](index.json).

