# Previewing the site locally

Run the redesign branch on your own machine, without merging it and without
touching the live site.

## 1. One-time setup

You need **Git** and **Ruby 3.x** (3.3 is what this was built with). Check with
`ruby -v` and `git --version`.

- **Windows:** install Ruby from <https://rubyinstaller.org> (choose the
  "Ruby+Devkit" build and accept the `ridk install` step), or use WSL.
- **macOS:** `brew install ruby`, then follow brew's note to add it to your PATH
  (the system Ruby is too old).
- **Linux/WSL:** `sudo apt install ruby-full build-essential zlib1g-dev`.

Then install Bundler if it's missing: `gem install bundler`.

## 2. Get the branch

```sh
git clone https://github.com/dscurrey/dscurrey.github.io.git
cd dscurrey.github.io
git checkout ccr-7c4330d5-q3wpkk
```

Already have a clone? Run `git fetch origin` then
`git checkout ccr-7c4330d5-q3wpkk` and `git pull`.

## 3. Install and serve

```sh
bundle install
bundle exec jekyll serve --livereload
```

Open <http://localhost:4000>. Stop it with `Ctrl+C`.

If `bundle exec jekyll` says the command is not found, use:

```sh
bundle exec ruby -S jekyll serve --livereload
```

`--livereload` refreshes the browser when you save a file.

## 4. What to edit while previewing

| To change | Edit |
|---|---|
| Name, tagline, social links, summary, status, hero rows, accent colours, hero style | `_config.yml` |
| Experience entries | `_data/experience.yml` |
| About paragraphs | `_data/about.yml` |
| Skills | `_data/skills.yml` |
| Layout / markup | `_layouts/default.html`, `_includes/*.html` |
| Styling | `_includes/css/main.css` |

**`_config.yml` is not reloaded automatically.** After changing it, stop the
server (`Ctrl+C`) and start it again. Edits to `_data/`, layouts, includes and
CSS are picked up on save.

## 5. Things worth testing

- **Dark mode:** use the Theme button, and also change your OS appearance with
  the toggle never clicked. Clear the saved choice with
  `localStorage.removeItem("theme")` in the browser console.
- **Mobile layout:** open DevTools (`F12`), toggle the device toolbar, try
  ~390px wide.
- **Print / CV:** `Ctrl+P` (or `Cmd+P`) should give a clean two-page layout.
- **Accent colour:** edit `color.accent` and `color.accent_dark` in
  `_config.yml`, restart, and compare. Original green option: `#208c71` (too
  faint on the light background; `#1a7a5e` passes contrast) with `#4cc9a6` for
  dark.
- **Hero style:** set `hero_style: large` or `compact` in `_config.yml`.
- **Email:** set `show_email: true` to show the contact row.

## 6. Preview on your phone (same Wi-Fi)

```sh
bundle exec jekyll serve --host 0.0.0.0
```

Then open `http://<your-computer's-LAN-IP>:4000` on the phone. Your OS firewall
may ask to allow Ruby. Don't use this on public Wi-Fi.

## Troubleshooting

- **`bundle install` fails building a gem on Windows:** rerun `ridk install`
  and choose the MSYS2 development toolchain option.
- **Port 4000 in use:** add `--port 4001`.
- **Fonts look different:** JetBrains Mono loads from Google Fonts, so you need
  to be online. Offline it falls back to a system monospace font.
- **`Address already in use` / stale page:** hard refresh (`Ctrl+Shift+R`).
- **Changes to `_config.yml` have no effect:** restart the server.

Generated files go to `_site/`, which is git-ignored.
