# ExtraReach redesign (local)

Local redesign + first weekly journal post for **ExtraReach** (Hector Royes / Carlos, chief designer). Offline-friendly static HTML/CSS—no build step, no trackers.

## Preview locally

From this folder:

```bash
cd /workspace/extrareach-redesign
python3 -m http.server 8080
```

Then open `http://localhost:8080/` (or open any `.html` file directly via `file://`).

## Images (Carlos)

Drop generated PNGs into `images/` using these exact names:

| File | Used on |
|------|---------|
| `images/extrareach-hero-passive-house.png` | Homepage hero |
| `images/extrareach-envelope-diagram.png` | Featured post card + post hero |
| `images/extrareach-interior-daylight.png` | Mid-article image in the weekly post |

Until the PNGs land, pages show a soft fallback placeholder (via `onerror`).

## Pages

- `index.html` — redesigned homepage
- `post-phius-2024-what-changed.html` — first weekly post (Sep 2026)
- `basics.html` / `journal.html` / `resources.html` — stubs with shared chrome
- `styles.css` — design system

## What changed vs live extrareach.com

| Live site | This redesign |
|-----------|----------------|
| Dark navy, sparse, text-only | Same navy editorial base, richer cards/hero/trust |
| System fonts, minimal hierarchy | Clear hierarchy, bordered cards, hover affordances |
| Nav links were `#` placeholders | Real local links across all pages |
| No images | Hero + envelope + interior image slots |
| Two January 2026 posts only | Those titles kept as older cards + new Sep 2026 weekly post |
| About/topics sidebar only | Trust card (Hector / planning-stage) + sidebar + CTAs |
| No mobile nav pattern | Compact header + hamburger menu under 640px |
| No weekly standards/incentives deep dive | Full first post with cited Phius / IRS / WA sources |

Still lean: one CSS file, tiny inline JS for mobile nav only, no third-party scripts or fonts.
