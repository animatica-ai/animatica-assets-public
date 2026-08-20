# animatica-assets-public

Assety 3D do pobrania - [animatica.ai](https://animatica.ai).

Kazdy asset zawiera geometrie, shading network i (jesli istnieje) rig
w natywnych formatach aplikacji oraz uniwersalne zrodla USD/FBX z teksturami.

## Pobieranie

Repo uzywa Git LFS - zainstaluj go przed klonowaniem:

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

| Asset | Wersja | Aplikacje | Licencja |
|---|---|---|---|
| [Test Cube](assets/test-cube/) | v004 | Blender, Maya, 3ds Max, Unreal Engine | wlasnosc Animatica (© Animatica) |

Lista maszynowa: [index.json](index.json).

