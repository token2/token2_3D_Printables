# token2_3D_Printables
3D Printable accessories for different Token2 Products - All in one Repo



# Desktop dock for the compact  smart card reader

A 3D-printable dock that turns the compact [T2SR](https://www.token2.com/products/token2-t2sr-compact-usb-nfc-and-smart-card-reader)  card reader into a desktop reader. It works with a mini-USB cable of any length.

The reader comes with a short stowable USB cable. This dock ignores that cable and uses the reader's **mini-USB port** instead. You plug in a standard mini-USB cable through a tunnel at the back of the dock. The dock holds the reader firmly. Once the cable is plugged in, the reader can't fall out, even if the dock is turned upside down.

<img width="600" alt="image" src="https://github.com/user-attachments/assets/82b7a4a3-9021-44cd-80e2-eeb2812093d0" />


## Features

- **Lip over the far edge.** On the edge opposite the USB port, a 5 mm lip covers the top of the reader. At the USB end, the mini-USB plug sits in a snug tunnel. Together they lock the reader in place once the cable is plugged in.
- **Open card slot.** The side with the card slot is left open, so a standard ISO/IEC 7810 ID-1 card (85.6 × 53.98 mm) goes in and comes out freely.
- **Card-side ridge.** A 1.2 mm ridge runs along the card side. It stops the reader being dragged out when a card is pulled. The card passes about 1 mm above it.
- **5° tilt towards the back.** Cards or keys placed on top slide back against the back stop instead of off the front.
- **Full-width back stop.** The back stop is the same height as the cable tunnel and runs the full width of the dock.
- **Recesses for rubber feet.** Four Ø10.5 × 1 mm recesses fit standard 8–10 mm self-adhesive bumpers. The feet are optional, since the dock also sits flat without them.
- **Light underside.** The wedge under the base is filled with a cell grid. It needs no supports, because each cell roof only bridges 8 mm.
- **Raised "token2.swiss" text** on the front edge.

| | |
|---|---|
| Overall size | 66 × 98.5 × 20 mm |
| Material | ~32 cm³ |
| Reader clearance | 0.15 mm per side |
| Cable tunnel | 10.5 × 7 mm, 10 mm long (for the mini-USB plug's moulded head) |

## Files

| File | Purpose |
|---|---|
| `compact_reader_desk_dock_v1.stl` | Ready to print |
 

## Printing

- **Orientation:** flat on its base, as exported.
- **Material:** PLA or PETG.
- **Settings:** 0.4 mm nozzle, 0.2 mm layers or finer (the text strokes are about 0.9 mm wide), 3 perimeters, 15–20 % infill.
- **Supports:** only the 5 mm front lip needs them. Use *supports touching the build plate only*, or print it without supports and lightly sand the lip's underside.
- **Two-colour text:** add a filament change at the layer where the text starts.

## Fit and tolerances: read this before printing

The reader is held tightly on purpose. Depending on your printer, filament and slicer settings, you may need to adjust the fit.

- **Under the lip.** In the reference print, the pocket under the lip grips the reader's edge tightly. That's intended, and it was kept. If your print is too tight to slide the reader under the lip, or too loose, change `LIP_GAP`:
  - Raise it (e.g. 0.2 → 0.3–0.4 mm) if it's too tight, or if the lip sagged because it was printed without supports.
  - Lower it (e.g. 0.1 mm) if the reader rattles.
- **Around the reader.** If the reader won't drop into the pocket, raise `CLR` from 0.15 to 0.2–0.25 mm. Printers that over-extrude usually need this.
- **Cable tunnel.** Moulded mini-USB plug heads vary in size. The tunnel fits heads up to 10.5 × 7 mm. If your plug doesn't fit, or wobbles, change `PLUG_W` and `PLUG_H`. A snug plug is what stops the reader tilting out at the USB end.
- **Card-side ridge.** If cards still drag the reader out, raise `RIDGE_H` to about 1.5 mm. The card will still clear it.

Print a test piece and adjust before printing the final dock.

## Assembly

1. Drop the reader into the pocket at the USB end (there's 5.4 mm of extra room there).
2. Slide it forward until its far edge is under the lip.
3. Push the mini-USB plug through the tunnel from the back and into the reader's port.
4. Optionally, stick rubber feet into the four recesses underneath.

To remove the reader, unplug the cable, slide the reader back and lift it out.

## Customising

All dimensions are parameters at the top of `reader_desk_dock_v11.py`:

| Parameter | Default | Meaning |
|---|---|---|
| `CLR` | 0.15 | Pocket clearance per side |
| `LIP_D` / `LIP_T` / `LIP_GAP` | 5.0 / 1.4 / 0.2 | Lip overhang, thickness, and gap above the reader |
| `SLIDE` | `LIP_D` + 0.4 | Extra pocket length at the USB end, so the reader can slide under the lip |
| `RIM_H` / `RIM` | 6.5 / 3.0 | Side wall height above the base / wall thickness |
| `RIDGE_H` / `RIDGE_W` | 1.2 / 1.6 | Card-side ridge height / width |
| `PLUG_W` / `PLUG_H` / `TUN_L` | 10.5 / 7.0 / 10 | Cable tunnel width / height / length |
| `TILT` | 5.0 | Tilt towards the back, in degrees |
| `BACKSTOP` | True | Full-width back stop at tunnel height |
| `BASE_T` / `MARGIN` | 3.0 / 10 | Base thickness / base margin around the walls |
| `FOOT_D` / `FOOT_T` | 10.5 / 1.0 | Rubber-foot recess diameter / depth |
| `LOGO_W` / `LOGO_H` / `LOGO_ROT` | 38 / 0.6 / 180 | Text width / height / rotation |

### Building from source

The script needs [CadQuery](https://github.com/CadQuery/cadquery) (Python 3):

```bash
pip install cadquery
mkdir -p out
python reader_desk_dock_v11.py out
```

It writes `reader_desk_dock_v11.step` and `reader_desk_dock_v11.stl` to `out/`.

The script expects these paths, relative to the folder you run it from:

- `work/tagline_polys.json`: the text outlines. Edit `LOGO_SVG_POLYS` if you keep the file somewhere else.
- `parts/p0.step` and `parts/p1.step`: the reader's two housing halves, split from the reader's STEP model. These are only used for the fit checks at the end of the script, which test reader overlap, the drop-in path and card clearance. If you don't have the reader model, remove those lines.

## Reader reference dimensions

These were taken from the reader's STEP model.

- Body: 39.9 × 66 × 7.8 mm, with corner radius ~4 mm.
- Mini-USB port: centred on one short edge, about 5.4 mm above the bottom.
- Card slot: on one long edge, about 2.1 mm above the bottom and 54 mm wide. An inserted card sticks out about 48 mm.
