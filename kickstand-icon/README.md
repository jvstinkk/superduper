# Kickstand app icon

The back of a bike resting on its kickstand: a bone-white wheel and frame stay, and an orange stand set 17° off vertical with its foot on the ground. Orange is the only accent, matching the app, where orange means "unlocked".

## Files

| Path | What it is |
| --- | --- |
| `layers/01-wheel.svg` | Wheel ring and hub |
| `layers/02-frame.svg` | Frame stay from the hub to the stand's pivot |
| `layers/03-stand.svg` | The kickstand and its foot (orange) |
| `layers/04-ground.svg` | Ground line (optional) |
| `layers/00-background.svg` | Asphalt gradient, only if you want the background as a layer |
| `layers-png/` | The same layers as 1024 × 1024 transparent PNGs |
| `preview.png` | Preview at several sizes, the watch circle and a light appearance |
| `kickstand-icon-1024.png` | Flat 1024 reference image |

Every layer is a 1024 × 1024 canvas with the art already in position, so dropping the layers in lines them up. Use the SVGs; the PNGs are a fallback.

## Set up in Icon Composer

1. Open Icon Composer (Xcode > Open Developer Tool > Icon Composer) and create a new document.
2. Set the document **Fill** to a linear gradient, `#26292E` at the top to `#0F1012` at the bottom. Skip `00-background.svg` unless you'd rather have it as a layer.
3. Drag the layers in as four groups, front to back:
   1. **Stand**: `03-stand.svg`
   2. **Frame**: `02-frame.svg`
   3. **Wheel**: `01-wheel.svg`
   4. **Ground**: `04-ground.svg`
4. Suggested starting point: Liquid Glass and specular on for Stand, Frame and Wheel; Ground with glass off at about 70% opacity; neutral shadow. Adjust to taste.
5. Check the watchOS preview. All the art sits inside the watch circle.

## Appearances

| Appearance | Fill | Wheel, frame | Ground | Stand |
| --- | --- | --- | --- | --- |
| Default and Dark (as designed) | `#26292E` → `#0F1012` | `#F4F2EE` | `#8C9198` | `#FF5B14` |
| Optional light | `#FFFFFF` → `#E9E6E0` | `#121314` | `#6B7077` | `#FF5B14` |

Icon Composer generates the Clear and Tinted looks. Check that the stand still stands out there; if it doesn't, raise its opacity in those appearances.

## Editing the geometry

- Canvas: 1024 × 1024. The art spans about 69% of the width.
- Wheel: centre (564.64, 497.44), outer radius 257.6, ring 67.2 thick, resting on the ground at y 755.04.
- Stand pivot: (224.16, 385.44). The stand is rotated −17° in its SVG; change that number to change the lean.
- Strokes are drawn as filled shapes (rounded rectangles and rings), so Liquid Glass picks up clean edges.
