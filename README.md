# PFP//STUDIO

A tiny browser tool that recolors the classic default social-media avatar — the
gray circle with a person silhouette — and lets you download the result as a
PNG. No sign-up, no uploads, no server. Everything is drawn and exported
locally in your browser.

**[Live demo →](#)** <!-- https://pratikmourya.github.io/PFP_STUDIO/ -->


## Features

- 🎨 Independent color control for the background and the person silhouette
- 🔢 Type any hex code directly, or pick from the color wheel
- ⚡ One-click random color combo
- 🖼️ Preset combinations to start from
- 📥 Free PNG export at 320 / 512 / 1024 / 2048px
- 📱 Responsive — works on phones, tablets, and desktop
- 🔒 Fully client-side: nothing you create is ever uploaded anywhere

## Usage

1. Open `index.html` in any modern browser (or visit the live demo above).
2. Adjust the **Background Colour** and **Person Colour** using the color
   wheel or by typing a hex code.
3. Pick an export resolution.
4. Click **Download PNG** to save your avatar.


## Tech

Plain HTML, CSS, and vanilla JavaScript. The avatar is an inline SVG that gets
recolored live and rasterized to a `<canvas>` for PNG export — no frameworks,
no build tools.

## Contributing

Issues and pull requests are welcome — new preset palettes, additional avatar
shapes, or accessibility improvements are all good candidates.

## License

MIT — see [LICENSE](LICENSE).
