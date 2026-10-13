# Design notes

Working notes for the site overhaul (not published; excluded in `_config.yml`).

## Deferred / to revisit
- **Hairline detail** (corner ticks / crosshair marks on the sheet, technical-drawing style): left out for now, **revisit later**.
- **Accent colour**: `#c8381a` (light) / `#ff7a50` (dark) kept for now; needs real-world testing. Alternatives: original green `#208c71`, deep blue.
- **End of redesign**: set `status` to "Experimenting with AI" (or similar) in `_config.yml`; currently a placeholder ("Rebuilding this site"). Summary is final (spec-sheet style).
- **Hero**: compact is the default; large is available via `hero_style: large` in `_config.yml`.
- **Portrait**: `img/profile.png` is a placeholder logo; replace with a real photo.
- **Experience wording**: corrections applied. Shorter bullets still to review.
- **Hero**: decide `summary` text, `status` text (both placeholders), and whether to rename Role; `show_email` is off by default.

## Where things live
- Content: `_data/experience.yml`, `_data/about.yml`, `_data/skills.yml`
- Settings (name, tagline, socials, hero, accent): `_config.yml`
- Build-generated: spec strip (REV, Jekyll version, counts) and "Last updated" stamp, both from the build time.
