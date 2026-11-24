# LUFFY PLAYZ — Portfolio

A premium, single-file portfolio for **LUFFY PLAYZ** (ScarFall 2.0 · Samrat rank · Asia server).
Rebuilt from the original project with a more advanced, high-end art direction: editorial
typography, champagne-gold accents, glass panels, refined motion and SVG iconography.

## Files

```
LUFFY-PLAYZ/
├── index.html      ← the whole site (HTML + CSS + JS, no build step)
├── netlify.toml    ← security + cache headers for Netlify
└── README.md
```

## Preview locally

Just open `index.html` in any browser. Or serve it:

```bash
python3 -m http.server 8080
# then visit http://localhost:8080
```

## Deploy

**Netlify** — drag the `LUFFY-PLAYZ` folder onto https://app.netlify.com/drop
(the included `netlify.toml` adds the headers automatically).

**GitHub Pages** — push the folder contents to a repo, then enable Pages on the
`main` branch (root). `index.html` is the entry point.

**Vercel** — import the repo, framework preset: *Other*, output directory: `.`

## What to edit

| What | Where |
|---|---|
| Brand / title | `<title>` and the `.brand-word` blocks in `index.html` |
| Social links | search for `ZENO-LUFFY` (YouTube) and `zeno.luffy.playz` (Instagram) |
| Contact email | search for `manngamingyt1@gmail.com` |
| Contact form | search for `formspree.io/f/` — replace `mdavykvq` with your own Formspree ID |
| Stats | `data-count` / `data-suffix` attributes |
| Skill percentages | the `.bar` rows (label, `%` text, and `data-val` on `.fill`) |
| Radar values | the `vals` array in the radar script (`[.96,.94,...]`) |
| Gallery | each `.g-item` button: `data-full` (lightbox image), `data-cap` (caption), and the `<img src>` |
| Avatar | the `<img>` inside `.d-img` |
| Accent colour | `--gold` / `--gold-2` in `:root` |
| Footer year | nothing — every `data-year` element (footer, nav, season labels) fills in the current year automatically |

## Design notes

- **Type**: Sora (display), Manrope (body), Instrument Serif (italic accents), JetBrains Mono (labels).
- **Palette**: near-black `#050506` with champagne gold `#D8B678` — no neon clutter.
- **Motion**: scroll reveals, count-ups, animated radar, magnetic buttons, card tilt,
  gold cursor on desktop. All animation respects `prefers-reduced-motion`.
- **Performance**: one file, no frameworks, lazy-loaded gallery images, GPU-friendly transforms.
- **Responsive**: tuned at 1080 / 860 / 600 px; full-screen mobile menu; touch-safe (no custom cursor).

## Notes

- The contact form posts to Formspree. Until you swap in your own form ID it will only
  work with the existing `mdavykvq` endpoint — test it once after deploying.
- Gallery photos are Unsplash placeholders. Replace them with real gameplay screenshots
  for the strongest result (keep the same `data-full` pattern for the lightbox).
