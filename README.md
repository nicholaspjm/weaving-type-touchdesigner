# Weaving Type

A TouchDesigner instrument that renders **text, images, and 3D geometry as drooping woven thread**. Feed it a word, a photo, or a piece of geometry and it stitches the shapes into a soft, hand-woven fabric of Bézier threads — with live look controls, gravity, 3D, and hands-on interaction.

It started as a port of [airfan003's WeavingType](https://airfan003.github.io/WeavingType/) (#Genuary) and grew into a full real-time instrument.

Download from this Repo or from [my pateron](https://www.patreon.com/c/PJCreations).

[Example Project Files Here](https://www.patreon.com/c/PJCreations)

---

## Requirements

- **TouchDesigner 2023.30000 or newer** (developed and tested on 2023.x and 2025.x builds).
- Non-Commercial or any Commercial licence — it uses standard operators only.

## Install

**Option A — add it to your palette (recommended)**
1. Copy `weaving_type.tox` into your TouchDesigner user palette folder:
   `Documents/Derivative/Palette/`
2. Restart TouchDesigner (or right-click the Palette browser → *Refresh*).
3. Drag **Weaving Type** from the Palette (`My Components`) into your project.

**Option B — drop it straight in**
- Drag `weaving_type.tox` from disk into any TouchDesigner network.

On first use, open the **Common** tab and enable **License accepted** to activate the tool.

---

## Quick start

1. Drop the component in and open its parameters.
2. On the **General** page, set **Source** to `Text` and type a word.
3. Tune **Weave** (spacing, weight, sag) and **Color** to taste.
4. Wire the component's TOP output wherever you need it.

## Inputs (General → Source)

| Source | What it does |
|---|---|
| **Text** | Type any word; pick font, weight, size, alignment. |
| **Image / TOP** | Feed a photo, logo, or mask — it weaves the shapes (and can sample the image's own colours). |
| **SOP / POP** | Pipe in 3D geometry — a shape or a particle system — and it weaves the form. |

## Controls (parameter pages)

- **General** — Source, all the text/font/layout controls, 3D (perspective, rotate, auto-spin), and output resolution.
- **Weave** — layers, thread spacing / weight / density, edge jitter, within- vs gap-sag, drape, seed.
- **Color** — mono / duo / tri-tone palette, or sample colours from the source; background colour + alpha.
- **Interact** — grab and pull the threads (see below).
- **Optimise** — scan resolution, curve segments, max threads, and **Liveupdate**.
- **Common** — licence acceptance, credit, version.

## Interaction

Open the built-in **interaction panel** and reach into the weave:

- **Input type** — *Mouse* or *TOP driver* (a moving blob / tracked position).
- **Interaction** — *Hover* (threads sag under the driver) or *Click-drag* (grab and pull, then spring back).
- **Pull** toggle — the grab signal for the TOP driver. Export a **pinch** channel to it and you can reach in and pull the weave around live, hands-free.
- **Radius / Strength** — grab size and pull amount.

## Tips

- **Liveupdate** rebuilds the entire weave every frame — leave it **off** for still text/images (fast). Only turn it on when the *source* is animated (live video / a moving TOP), and raise **Update frames** to soften the load.
- For heavy inputs, drop **Sample density** to reduce the underlying point count (keeps the whole image, just coarser), rather than cropping with **Max threads**.

---

## Credits

- Built by **Nicholas Marriott** ([@nicholaspjm](https://github.com/nicholaspjm)).
- Original concept and look: **airfan003 — [WeavingType](https://airfan003.github.io/WeavingType/)**.

## Licence

Free to use in any personal or commercial project — see [`LICENSE`](LICENSE). In short: use it anywhere, don't resell or repackage it, and keep the credit. This repository is the official source.

## Contributing

Issues and pull requests are welcome — see [`CONTRIBUTING.md`](CONTRIBUTING.md).
