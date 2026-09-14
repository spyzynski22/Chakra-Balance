# The Seven Centers of Light

An interactive, single-page guide to the seven chakras — built for [Purple Light Lounge](https://www.skool.com/purple-light-lounge-6229/about).

**[View it live →](#)** *(add your GitHub Pages URL here once deployed)*

## What it does

For each of the seven chakras, the page walks through:

- Element and physical body associations
- What the chakra governs
- What it feels like balanced vs. imbalanced (under-active and over-active)
- Where imbalance often comes from
- A journal prompt
- A simple practice to help rebalance it
- An affirmation
- A healing sound frequency (396–963 Hz) you can play right in the browser

A sticky rainbow rail on the side tracks your scroll position, and a "Join Purple Light Lounge" link appears at the top and bottom.

## Tech

Everything lives in a single `index.html` file — no build step, no dependencies to install:

- Plain HTML/CSS/JS
- Google Fonts (Cormorant Garamond + Jost) loaded via `@import`
- The prism/crystal hero graphic is generated on load with inline SVG
- Sound tones are generated live with the Web Audio API — no audio files needed

## Deploying to GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, choose the `main` branch and `/ (root)` folder.
4. Save — your page will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Editing content

All the chakra content lives in one place: the `CHAKRAS` array near the top of the second `<script>` block in `index.html`. Each entry is a plain object — edit any field (`meaning`, `balanced`, `imbalanced`, `rootCause`, `journal`, `practice`, `affirmation`, `freq`, etc.) and the page rebuilds itself from that data on load.

To change the community link, search `index.html` for `skool.com` — it appears twice (top CTA and footer CTA).

## Notes

- Headphones are recommended for the sound frequencies (there's a note on the page for this).
- Tested in modern Chrome, Safari, and Firefox. The Web Audio API requires a user gesture (tapping play) before sound will start — this is a browser requirement, not a bug.
