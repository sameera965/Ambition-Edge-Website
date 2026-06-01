# Ambition Edge

The official website of **Ambition Edge**, a private business transformation practice based in Calgary, working with service-based businesses worldwide.

Founded by Sameera Abdullah. Operated by **SAAAH Limited** (Federal Corporation 1456848-6).

---

## What this repo contains

A static, three-page website built in vanilla HTML, CSS, and JavaScript. No build step. No frameworks. Open any HTML file in a browser and it works.

```
.
├── home.html                       Landing page
├── services.html                   Services and pricing (5 tiers)
├── book.html                       Diagnostic Session booking page
├── hero-video.mp4                  Hero background video (~1.9 MB, compressed)
├── founder.jpg                     Founder portrait used in the home page
├── Ambition Edge Logo (6).png      White-style logo (used over the dark hero)
├── Ambition Edge Logo (2).png      Green-style logo (used on the scrolled nav and footer)
└── README.md                       This file
```

**Internal-only documents** (not part of the public site, do not deploy):
`Founding Client Agreement.docx`, `Pricing Rollout Plan.docx`, `Discovery Call Playbook.docx`, `Lead Pipeline Dashboard.xlsx`, and other strategy docs. If publishing this repo publicly, move these to a private folder or `.gitignore` them.

---

## Preview locally

Double-click `home.html`. It will open in your default browser and render exactly as it will on the live site. All three pages link to each other via relative paths.

---

## Deploy to a live URL (free, ~5 minutes)

The fastest path is **Netlify Drop**.

1. Go to [https://app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag this folder onto the page.
3. Netlify will give you a live URL within seconds, in the format `https://something.netlify.app`.
4. Inside Netlify, you can connect your own domain (e.g. `ambitionedge.ca`) under **Site Settings → Domain management**.

Other equally easy options: GitHub Pages, Vercel, Cloudflare Pages. All free for a small static site like this.

---

## Editing the pages

Each HTML file is fully self-contained: HTML, CSS, and JavaScript live in one file. Open in any text editor (Notepad works, VS Code is nicer) and edit the text directly. Search for the words you want to change.

### Brand colours (CSS variables near the top of each HTML file)

| Token | Hex |
|---|---|
| `--forest` | `#0B3D2E` |
| `--forest-deep` | `#072920` |
| `--forest-soft` | `#14513F` |
| `--gold` | `#C9A961` |
| `--gold-deep` | `#A8893F` |
| `--gold-soft` | `#E8D9B0` |
| `--ivory` | `#F8F5EE` |
| `--cream` | `#EFE9DA` |

### Fonts

- **Fraunces** (serif) — used for headings and display type
- **Inter** (sans-serif) — used for body copy
- Both loaded via Google Fonts in each HTML `<head>`

### Replacing the hero video

Drop any `.mp4` file in this folder, named `hero-video.mp4`, replacing the existing one. Keep the file under ~3 MB so the page loads fast. Compress with `ffmpeg` if needed:

```bash
ffmpeg -i input.mp4 -vcodec libx264 -crf 30 -vf "scale=1920:-2" -an -movflags +faststart hero-video.mp4
```

### Changing the founder photo

Replace `founder.jpg` with any portrait. Vertical orientation (4:5 ratio) renders best. The website's home page references it directly.

### Updating the contact email

Search any HTML file for `contactambitionedge` and replace site-wide.

---

## Pricing (current state of the site)

The site is currently in **Founding Client phase**. Prices shown:

- **Diagnostic Session**: CAD $750 founding rate (list $2,500), limited to first 8 clients
- **90-Day Transformation**: CAD $7,500 founding ($2,500/mo × 3, list $18,000)
- **Strategic Retainer**: CAD $3,000/mo founding (list $6,500/mo)

When the founding cohort fills, update prices in `services.html` (tier cards) and `book.html` (summary panel), and remove the founding banner in the `.ladder-head` section of `services.html`. See `Pricing Rollout Plan.docx` for full rollout milestones.

---

## Browser support

Tested on current Chrome, Safari, Firefox, and Edge. The hero video falls back to a still image via the `<img>` inside `<video>` if the browser cannot play MP4. All third-party stock images use the `onerror` JavaScript fallback to a branded gradient block if any image fails to load.

---

## Tech notes

- **No build step.** No npm, no bundler, no compiler. Open and edit.
- **No third-party JavaScript.** Vanilla JS only (sticky nav, tab switcher, year footer, image fallback).
- **No tracking or analytics** installed by default. Add Google Analytics, Plausible, or Fathom if needed.
- **Responsive** down to ~360px wide. Tested on iPhone and standard desktop sizes.
- **Accessibility**: semantic HTML5 elements, alt text on all images, sufficient colour contrast in the brand palette.

---

## License and copyright

© 2026 SAAAH Limited. All rights reserved. **Ambition Edge** and the **A.R.I.F. Method™** are trademarks of SAAAH Limited.

This repository and its contents are proprietary. Do not reproduce, redistribute, or use in derivative work without written permission.

---

## Contact

- **Email**: contactambitionedge@gmail.com
- **Phone**: +1 403-796-5389
- **LinkedIn**: [Sameera Abdullah](https://www.linkedin.com/in/sameera-abdullah-80aa6548/)
- **Location**: Calgary, Alberta, Canada
