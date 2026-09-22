# Little Art Studio

An English-language preschool coloring app with a sticker-book theme.

- **Pencil** always stays inside the closed outline where a stroke begins. Start inside a shape, not on its outline. On blank paper it draws freely.
- **Brush** draws freely across outlines.
- **Fill** combines the old bucket and roller: tap a closed area to fill it with the selected texture. Choose **Smooth** for a plain color.
- The **Colors** and **Textures** palettes are always visible. Swipe sideways to see additional choices on smaller screens.
- **Grass** and **Night sky** use their natural colors; other tintable materials use the selected paint color.
- **Stickers** offers 18 pictures. Select one and tap the paper repeatedly to place copies. Undo, Redo, erasing, and PNG export include placed stickers.
- **Undo** removes the last action; **Redo** restores it. **Save** stores a picture locally in this browser. Use More → My pictures to download or share it.
- Sound effects use Web Audio. English speech uses an available system voice; it is not a recorded child voice and voice availability varies by device.

## Hosting

Static GitHub Pages app. Publish these files from `main` at `/(root)`. No build or API key is needed. The service worker supports offline app loading after a successful online visit. Increment its cache version when updating files.

## Verification

Automated Chrome tests cover pencil clipping, free brush strokes, textured bucket fill, Undo/Redo, 18 stamp stickers, saving, English dialogs, desktop/mobile layouts, and offline loading under `/g/`. Physical iPad/Safari and device speech have not been tested.
