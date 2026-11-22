# token2_3D_Printables
3D Printable accessories for different Token2 Products - All in one Repo



# 1 . Desktop dock for the compact  smart card reader

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

 

 

## Reader reference dimensions

These were taken from the reader's STEP model.

- Body: 39.9 × 66 × 7.8 mm, with corner radius ~4 mm.
- Mini-USB port: centred on one short edge, about 5.4 mm above the bottom.
- Card slot: on one long edge, about 2.1 mm above the bottom and 54 mm wide. An inserted card sticks out about 48 mm.

# 2. Bio3 Desk Holder

A 3D-printable desktop holder for the Token2 Bio3 FIDO2 key. It turns the key into a desk fingerprint reader: the key sits in a weighted base at the end of a USB-A extension cable, sensor facing up, so you touch it on the desk instead of reaching for a port.

 <img width="400" alt="image" src="https://github.com/user-attachments/assets/ccff04b1-5150-454e-a309-738f2b631db7" />


## Sample setup

<img width="400" alt="image" src="https://github.com/user-attachments/assets/c10da5f7-7665-42c2-bd20-d5dc12a2fe02" />
 

## Features

- **Half-proud seat.** The key sits 3.2 mm deep, so its top half and the whole fingerprint sensor stand clear of the base.
- **Front hood.** A cap covers the USB-C plug and the first 7 mm of the key body, which stops the key moving forward and holds its nose down.
- **Rear snap clasps.** Two spring arms end in hooks that click behind the rear corners of the key, either side of the USB-A plug, so pulling the cable cannot drag the key out.
- **Ballast.** Ten pockets on the underside take standard M8 hex nuts (about 50 g of steel in total).
- **Feet.** Four recesses for 8 mm stick-on rubber feet.
- **One piece, no supports.**

| | |
|---|---|
| Footprint | 60.8 × 90 mm |
| Height | 11.7 mm deck, 16.9 mm at the hood |
| Key seat | 18.7 mm wide (0.2 mm clearance per side) |
| Nut pockets | 10 × M8, 13.3 mm across flats, 7 mm deep |

 <img width="400" alt="image" src="https://github.com/user-attachments/assets/9ad7e7e0-d8d1-4ec7-8d5f-fd88604e05fd" />


## What you need

- 1 × printed `bio3_desk_holder-v2.stl`
- 1 × USB-A extension cable (male to female)
- 10 × M8 hex nuts (13 mm across flats, 6.5–6.8 mm thick)
- 4 × self-adhesive rubber feet, 8 mm diameter
- Optional: a drop of glue or a strip of tape if the nuts sit loose

## Printing

- Print flat, as oriented in the file. No supports; all overhangs are short bridges.
- PETG is recommended. The clasp arms flex about 3 mm each time the key goes in or out, and PLA is more likely to crack over time.
- 0.2 mm layers, 3–4 walls, high infill. The plastic is roughly half of the final weight.

## Assembly

1. Press the M8 nuts into the pockets on the underside.
2. Stick the rubber feet into the four corner recesses.
3. Slide the key in from the back, USB-C end first and sensor up, until the clasps click behind it. Help the arms apart with a fingernail if needed.
4. Plug the USB-A extension onto the key.

To remove the key, unplug the extension, spread the two arms and slide the key back.

## Fit notes

- The model was built from the dimensional drawing of the key (body 33.1 × 18.3 × 6.4 mm).
- The hooks sit between the key body and the face of the extension socket. They need about 1.5–2 mm of gap there; an extension that sits flush against the key body will not seat fully.
- The rear notch takes an extension head up to about 18 mm wide.

 <img width="400" alt="image" src="https://github.com/user-attachments/assets/7cd4c895-42a2-495d-9ff8-d4b882598a7b" />


 

## Files

| File | Contents |
|---|---|
| `bio3_desk_holder-v2.stl` | Print-ready model |
 

The key and extension shown in the renders are simplified stand-ins for illustration.
