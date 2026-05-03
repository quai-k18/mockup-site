# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Static HTML mockup site for **La Fenêtre**, an artisanal ice cream shop (glacier) at Port de Morgat, Crozon, Brittany. Five fully self-contained single-file mockups exploring different visual directions for the same landing page.

No build step, no dependencies, no package manager. Open any `.html` file directly in a browser.

## File structure

Each file is a complete standalone page — all CSS is inline in `<style>` tags, no external stylesheets or scripts:

| File | Style direction |
|---|---|
| `index-style1-v2.html` | Warm editorial serif — Cormorant Garamond + Spectral, cream/teal palette |
| `index-style2-v2.html` | Summery vintage postcard — Cormorant + Playfair, sandy paper texture with SVG noise |
| `index-style3-v2.html` | Modern bold — Bricolage Grotesque + DM Sans, neon pink accents, playful |
| `index-style4.html` | Minimal luxury — Tenor Sans + Manrope, bone/teal, fixed nav, high whitespace |
| `index-style5.html` | Coastal festive — Sigmar + DM Sans + Caveat, midnight background, vivid neon palette |

## Design constants across styles

All five files share the same brand anchors:
- Brand name: **La Fenêtre**
- Accent color: `--teal: #0E4F58` (present in every palette)
- Language: French throughout
- Section structure: nav → hero → flavors/menu → about → visit/contact

## Deployment & index.html

The site is deployed via GitHub Pages. `index.html` is a style-picker landing page shared directly with non-technical stakeholders so they can choose a visual direction. Keep it clear and self-explanatory — no jargon, no instructions required. Stakeholders access it via a public URL; they do not clone the repo.

## Git commits

- Messages must be short (a few words)
- No reference to Claude, any LLM, or AI tools — write as if a human authored every commit

## Conventions

- CSS custom properties (`--var`) define the palette at `:root`; edit colors there, not inline
- Typography uses `.display`, `.sc` (small caps), and/or `.serif-italic` utility classes to switch font families on specific elements
- Google Fonts are loaded via `<link>` preconnect in `<head>`; to change a font, update both the `<link href>` URL and the corresponding CSS declaration
- Images are referenced as relative paths (e.g. `photo-hero.jpg`) — no images are committed; placeholders are expected to be swapped in production
