# Little Art Studio

A preschool coloring app hosted on GitHub Pages.

- Pencil stays inside the closed outline where a stroke starts. Brush paints freely.
- Fill uses either a solid color or the selected fixed-color texture.
- Fourteen paint colors and 27 textures, plus Smooth, open in large, scrollable palettes.
- Thirty-six named stickers; imported stickers and pictures persist in this browser.
- Remove imported items from the library with the × button. Restore removed imports brings them back.
- Opening a picture starts a new document with clean layers. Imported pictures keep their original proportions. Blank paper follows the current screen orientation.
- Small, Medium and Large sizes for pencil, brush and eraser are in the compact bottom dock.
- Ten Undo/Redo steps use canvas tile snapshots with one stored state per tile.
- Save stores work locally. More → My pictures downloads or shares saved work.
- Clearing browser site data removes local saved work and imports; they do not sync between devices.

## Hosting
Publish the root of main with GitHub Pages. No build or API key is required. Service-worker caching supports offline use after a complete online visit.

## Validation
Chrome tests cover portrait layouts, import proportions, clean new documents, recoverable import removal, ten full-canvas undo/redo steps, pencil clipping, free brush strokes, texture fill, stickers and offline loading. Physical iPad/Safari testing remains device-dependent.

English vocabulary uses generated Dylan preset audio (Higgsfield Seed Audio), bundled locally for consistent speech and offline playback. No API key or runtime speech service is needed. Sound off and page hiding stop narration; rapid selections replace the previous word.

v14: imported documents use a consistent 1600-pixel longest side even for tiny sources, keeping brush sizes usable. High-quality image resampling and 100–400% view zoom with explicit Move mode. Zoom never resamples the drawing or clears undo history. Low-resolution originals cannot regain missing detail through enlargement.
