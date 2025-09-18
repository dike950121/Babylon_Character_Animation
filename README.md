Babylon Mixamo Sit Scene
------------------------

Contents:
  index.html
  assets/
    character.glb
  editor-project/   (optional)
  blender/          (optional)

How to run:
  1) From the project root run a local server:
     python -m http.server 8000
  2) Open http://localhost:8000/index.html

If you need to edit animations:
  - Open the provided character.glb in Blender (see blender/ for .blend if provided)
  - Or import the glb into Babylon.js Editor (v5.x), test animation clips, re-export.

Notes:
  - To tweak which clip is used for "talk" or "shift" edit the regex strings in index.html:
      /talk|idle/i   and  /shift|fidget|adjust|pose/i
  - If you prefer to use a provided bench model, replace the createBench() call with:
      BABYLON.SceneLoader.Append('assets/', 'bench.glb', scene, ...);

Optional artifacts: blender/character.blend (if used), editor-project/ (Editor saved scene)
