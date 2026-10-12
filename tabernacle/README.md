# Mishkan: Tabernacle Explorer

An interactive 3D model of the Tabernacle described in Exodus 25–40, built with three.js.
It is one self-contained file, `index.html`, separate from the Support Fins app. There is
no build step, and every texture is generated in the browser, so there are no assets to
download.

## Run it

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000 --directory tabernacle   # http://localhost:8000/
```

It needs WebGL 2 and a connection to `cdn.jsdelivr.net`, where three.js r160 loads from.

## What's in it

- **Three ways to explore.**
  - **Guided tour:** 16 camera stops that follow a priest's path from the gate to the
    mercy seat, with narration.
  - **Walk:** first-person on foot. WASD and mouse on desktop; a joystick and drag-to-look
    on touch screens. Collisions stop you at walls and furniture, and the screens roll up
    as you approach.
  - **Aerial:** an orbit view.
- **Floating labels.** Every piece has a label in English and Hebrew. Labels hide behind
  walls, thin out when they would overlap, and expand when you walk up to them. Opening one
  shows its scripture references, dimensions in cubits and metres, materials, a KJV quote,
  and its meaning.
- **Motion graphics.**
  - An animated title sequence.
  - Title cards when you enter the court, the Holy Place or the Most Holy Place.
  - Dimension lines that draw themselves around the selected object.
  - Narration that reveals word by word.
- **Scene controls.**
  - The four coverings can be lifted apart to show each layer, or removed.
  - The veil can be torn from top to bottom (Matthew 27:51).
  - A day/night cycle. At night the pillar of cloud becomes a pillar of fire and the
    camp's fires come out.
- **Detail.**
  - The court: 60 pillars with silver capitals, bronze sockets, cords and pegs, and linen
    hangings that move in the wind.
  - The tent: 48 gilded boards on 96 silver sockets with their bars.
  - The furnishings, modelled from the text: the bronze altar with its horns, grating and
    fire; the laver; the table with twelve loaves; the seven-branched lampstand with
    almond cups; the incense altar; and the Ark with two cherubim.
  - The twelve tribes camped by their standards (Numbers 2).
- **Automatic quality.** The starting tier (Low, Medium, High or Ultra) comes from the GPU,
  memory and device type. After that, the measured frame rate adjusts resolution, shadows,
  bloom, ambient occlusion, anti-aliasing and the cloud's raymarch steps while you explore.
  You can also pick a tier yourself in the quality menu.

## Sources and assumptions

The layout follows a common reconstruction: the tent stands in the western half of the
court, the Ark sits at the centre of the western square, and the altar stands in the
eastern square. Scripture gives no size for the lampstand or the laver, or for the
thickness of the boards, so those use traditional proportions. One cubit is taken as 18 in
(45.72 cm). The camp is drawn compressed, and the tribal flag colours follow later
rabbinic tradition (Numbers Rabbah 2:7). Quotations are from the King James Version.
