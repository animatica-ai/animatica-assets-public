# Example scenes for the Animatica Blender addon

The addon's **Try an example** menu is built from this folder. Every `.blend`
here is an example: add one and it appears in the menu, delete one and it goes.
There is no manifest and no addon release involved.

- `<name>.blend` is the scene, stored in Git LFS. The addon checks each download
  against the LFS pointer's sha256.
- `<name>.json` (optional) is what the menu shows before the file is
  downloaded: `title`, `tier` and `order` (the menu's grouping and order),
  `seconds`, `prompt`, `lesson`, `character`, `credit`. Without one, the file
  name stands in.

The scenes are built by `tools/build_examples.py` in
[animatica-blender-plugin](https://github.com/animatica-ai/animatica-blender-plugin),
which writes both files into this folder.
