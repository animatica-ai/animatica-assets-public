# Test Cube

Wersja **v003** (2026-08-20). Jednostki: meters.

weryfikacja pelnego cyklu pipeline

![podglad](preview/thumbnail.png)

## Zawartosc

| Aplikacja | Folder | Rig |
|---|---|---|
| uniwersalne | source/ (USD + FBX + tekstury) | - |
| Blender | blender/ | brak |
| Maya | maya/ | brak |
| 3ds Max | max/ | brak |

## Otwieranie

Zip z Releases rozpakuj w calosci - sciezki do tekstur sa wzgledne i zakladaja
ze `source/` lezy obok folderow aplikacji.

- **Blender** - otworz plik z `blender/`. Tekstury sa podlinkowane sciezkami
  wzglednymi, wiec dzialaja od razu. Nie przenos folderu `source/`.
- **Maya** - najpierw ustaw projekt (File > Set Project) na folder `maya/`,
  dopiero potem otworz scene. Tekstury rozwiazuja sie przez projekt.
- **3ds Max** - najpierw ustaw projekt (File > Project > Set Active Project)
  na folder `max/`, dopiero potem otworz scene.
- **Inne programy** - uzyj `source/` (USD albo FBX) i tekstur z `source/textures/`.

Tekstury sa w konwencji PBR Metallic-Roughness. Kanal `Normal` to normalne
OpenGL (Blender, Maya, Houdini), `NormalDX` to DirectX (3ds Max, Unreal).

