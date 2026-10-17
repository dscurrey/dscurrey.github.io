# Design notes

Working notes for the site overhaul (not published; excluded in `_config.yml`).

## Deferred / to revisit
- **Hairline detail** (corner ticks / crosshair marks on the sheet, technical-drawing style): left out for now, **revisit later**.
- **Accent colour**: vermilion `#c8381a` (light) / `#ff7a50` (dark) chosen. Alternatives: original green `#208c71`, deep blue.
- **Status**: set to "Experimenting with AI" (final for the redesign); edit `status` in `_config.yml` to change.
- **Hero rows**: Discipline dropped. Experience is build-calculated from `since:`.
- **Future**: may switch accent to original green (`#208c71`) with a lighter dark-theme equivalent.
- **Hero**: compact is the default; large is available via `hero_style: large` in `_config.yml`.
- **Portrait**: `img/profile.png` is a placeholder logo; replace with a real photo.
- **Experience wording**: shortened bullets applied.
- **Hero**: decide `summary` text, `status` text (both placeholders), and whether to rename Role; `show_email` is off by default.

## Where things live
- Content: `_data/experience.yml`, `_data/about.yml`, `_data/skills.yml`
- Settings (name, tagline, socials, hero, accent): `_config.yml`
- Build-generated: spec strip (REV, Jekyll version, counts) and "Last updated" stamp, both from the build time.
