# Design notes

Working notes for the site overhaul (not published; excluded in `_config.yml`).

## Deferred / to revisit
- **Hairline detail** (corner ticks / crosshair marks on the sheet, technical-drawing style): left out for now, **revisit later**.
- **Accent colour**: `#c8381a` (light) / `#ff7a50` (dark) kept for now; needs real-world testing. Alternatives: original green `#208c71`, deep blue.
- **Hero**: compact is the default; large is available via `hero_style: large` in `_config.yml`.
- **Portrait**: `img/profile.png` is a placeholder logo; replace with a real photo.
- **Experience wording**: corrections proposed and awaiting approval; shorter bullets after that.

## Where things live
- Content: `_data/experience.yml`, `_data/about.yml`, `_data/skills.yml`
- Settings (name, tagline, socials, hero, accent): `_config.yml`
- Build-generated: spec strip (REV, Jekyll version, counts) and "Last updated" stamp, both from the build time.
