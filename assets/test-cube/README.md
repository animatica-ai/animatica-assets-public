# Test Cube

Wersja **v004** (2026-08-20). Jednostki: meters.

USD z pelnym shadingiem

![podglad](preview/thumbnail.png)

## Zawartosc

| Aplikacja | Folder | Rig |
|---|---|---|
| uniwersalne | source/ (USD z shadingiem + FBX + tekstury) | - |
| Blender | blender/ | brak |
| Maya | maya/ | brak |
| 3ds Max | max/ | brak |
| Unreal Engine 5.8.1 | unreal/ | brak |

## Otwieranie

Zip z Releases rozpakuj w calosci - sciezki do tekstur sa wzgledne i zakladaja
ze `source/` lezy obok folderow aplikacji.

- **Blender** - otworz plik z `blender/`. Tekstury sa podlinkowane sciezkami
  wzglednymi, wiec dzialaja od razu. Nie przenos folderu `source/`.
- **Maya** - najpierw ustaw projekt (File > Set Project) na folder `maya/`,
  dopiero potem otworz scene. Tekstury rozwiazuja sie przez projekt.
- **3ds Max** - najpierw ustaw projekt (File > Project > Set Active Project)
  na folder `max/`, dopiero potem otworz scene.
- **Unreal Engine** - skopiuj zawartosc `unreal/Content/` do folderu `Content/`
  swojego projektu. Pliki `.uasset` sa wersjonowane: otworza sie w silniku
  w wersji z tabeli powyzej albo nowszej, ale nie w starszej. Jesli potrzebujesz
  starszej wersji, zaimportuj `source/` samodzielnie.
- **Houdini, Omniverse i reszta** - otworz `source/<asset>.usd`. USD ma
  juz podpiety shading (`UsdPreviewSurface` + tekstury, sciezki wzgledne),
  wiec nie trzeba niczego podpinac recznie. Skopiuj caly folder `source/`.

Tekstury sa w konwencji PBR Metallic-Roughness. Kanal `Normal` to normalne
OpenGL (Blender, Maya, Houdini), `NormalDX` to DirectX (3ds Max, Unreal).

Uwaga dla Mayi: jej importer USD ignoruje `sourceColorSpace` i ustawia wszystkim
teksturom sRGB. W Mayi uzywaj gotowej sceny z `maya/` - ma poprawny color space.

