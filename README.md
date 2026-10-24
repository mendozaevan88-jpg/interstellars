# Evan — socials, covers & photos

A single-page personal site for Evanescence "Evan" Mendoza. It links to his social accounts, shows his Creep guitar cover and has a swipeable photo gallery. It is one self-contained HTML file with no build step and no dependencies.

## Features

- Light silver design with a frosted top bar and a bracketed "[ Get in touch ]" button
- Hero headline over an animated ribbon wave, drawn on a `<canvas>`, that bends toward the cursor
- Scroll-driven 3D scene: a tilted board where the Instagram, TikTok, X and Facebook cards rise up one by one as you scroll. Each card is a working link.
- A tilted video card for the Creep guitar cover that straightens on hover and opens TikTok
- Photo gallery you can swipe on a phone, drag with a mouse, or step through with the arrow buttons and the left and right arrow keys
- Responsive down to phone size, with visible keyboard focus and support for the `prefers-reduced-motion` setting

## Run it locally

1. Download or clone this repository.
2. Open `index.html` in any modern browser.

The page loads the Inter font from Google Fonts. Without an internet connection it falls back to your system sans-serif.

## Publish with GitHub Pages

1. Push `index.html`, `README.md` and `LICENSE` to a GitHub repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick your main branch and the `/ (root)` folder, then save.
4. Your site goes live at `https://<your-username>.github.io/<repository-name>/` after a minute or two.

## Customize

Everything lives in `index.html`.

| To change | Look for |
| --- | --- |
| Colors | The `:root` variables at the top of the `<style>` block (`--mag`, `--blu` and `--cor` are the card colors) |
| Text and links | The `<section>` blocks in the `<body>`. The social links appear twice, in the card board and in the "Say hi." list |
| Photos | The `const I = {...}` object near the bottom. Each image is embedded as base64, so replace the data string or use a file path such as `"photos/me.jpg"` |
| Ribbon wave | The `rib()` function |
| Card board motion | The `frame()` function, which sets the board tilt and how far each card lifts |

## Credits

- Design and motion inspired by the "TIDY" website demo shown in the video "I Tested Figma" (watermarked Code With Me). This is an independent recreation. No code, models or footage from that site are used.
- Font: [Inter](https://fonts.google.com/specimen/Inter), under the SIL Open Font License.

## License

The code is released under the [MIT License](LICENSE).

The photos embedded in the page are personal photos of the site owner and are **not** covered by the MIT License. All rights reserved. Please don't reuse them without permission. If you fork this project, replace them with your own.
