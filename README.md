# Little Art Studio

An English-language preschool coloring app with a sticker-book theme.

- **Pencil** always stays inside the closed outline where a stroke begins. Start inside a shape, not on its outline. On blank paper it draws freely.
- **Brush** draws freely across outlines.
- **Fill** combines the old bucket and roller: tap a closed area to fill it with the selected texture. Choose **Smooth** for a plain color.
- The **Colors** and **Textures** palettes are always visible. Paint colors have larger 46–52 px buttons. Swipe sideways to see additional choices on smaller screens.
- All textures have fixed material colors, including crayon, grass, clouds, night sky, sand, wood, hearts and stars. Choose **Smooth** to draw or fill with a selected paint color.
- **Stickers** offers 36 pictures in a compact four-column grid with vertical-only scrolling. Select one and tap the paper repeatedly to place copies. Undo, Redo, erasing, and PNG export include placed stickers.
- **Undo** removes the last action; **Redo** restores it. **Save** stores a picture locally in this browser. Use More → My pictures to download or share it.
- Sound effects use Web Audio. English speech uses an available system voice; it is not a recorded child voice and voice availability varies by device.

## Hosting

Static GitHub Pages app. Publish these files from `main` at `/(root)`. No build or API key is needed. The service worker supports offline app loading after a successful online visit. Increment its cache version when updating files.

## Verification

Automated Chrome tests cover pencil clipping, free brush strokes, textured bucket fill, Undo/Redo, 18 stamp stickers, saving, English dialogs, desktop/mobile layouts, and offline loading under `/g/`. Physical iPad/Safari and device speech have not been tested.

## New controls and import library

- Size offers inline Small, Medium and Large options for Pencil, Brush and Eraser, remembered separately during the session.
- Import stickers supports PNG/JPG/WebP and keeps transparency and aspect ratio. Imported stickers and pictures are stored in IndexedDB and appear in their pickers on subsequent visits in the same browser. Clearing site data removes this library; it does not sync between devices.
- More no longer includes Turn photo into outlines or New blank picture. Blank paper remains.
- Choosing a built-in sticker speaks its English name with Sound on. English system speech prefers a young/male voice and uses a youthful pitch fallback; it is not a recorded child voice.
- Drawing uses filtered noise to simulate pencil-on-paper, brush and eraser friction, following pointer movement and stopping on release, cancellation or loss of focus.
- Additional automated tests cover all three sizes, per-tool size recall, sticker speech dispatch, friction start/stop, transparent imports, import undo and import persistence after reload.

The texture picker shows eight familiar preschool materials and shapes, plus Smooth for plain colors. Linen, Watercolor and Candy are no longer offered.

Texture swatches and rows match the color palette dimensions on desktop, mobile and landscape. Eighteen additional named vector stickers bring the collection to 36.

Drawing performance: reuse outline masks for repeated strokes, crop masking to the brush area, cache texture patterns and friction audio samples, and use direct drawing for unclipped plain brushes. Outline changes invalidate cached regions. Color and Texture controls now expand on demand and close after a selection. Selecting textures speaks their English names. See textures-preview.html for 30 proposed patterns to choose from.

## Selected textures

The user-selected 26 preview patterns are now available in the app, with matching fixed colors and spoken English names: Grass, Clouds, Night sky, Sand, Wood, Water, Leaves, Flowers, Rainbow, Snow, Rain, Bubbles, Bricks, Fish scales, Fur, Feathers, Hearts, Stars, Dots, Stripes, Checks, Honeycomb, Sprinkles, Orange, Watermelon, Mud. Smooth remains available for solid paint. SVG tiles are decoded once at startup and cached for drawing; all artwork is inline for offline use.
