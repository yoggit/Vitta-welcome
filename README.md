# Vitta — welcome page

The public landing page for **Vitta · Vibe, Value & Virtue of Money**, a private
financial-literacy app for curious kids.

- **Live:** https://yoggit.github.io/Vitta-welcome/
- **The app:** https://vitta-dhaara.web.app

A single self-contained `index.html` — no build step, no dependencies. Pushing to
`main` is the deploy.

## Conventions shared with the sibling landing pages

All of these pages live on the one `yoggit.github.io` origin, so they share
`localStorage`:

- **Theme key is `apps-theme`.** One light/dark choice follows a visitor across the
  family. Each page still renders its own palette; the key only stores the choice.
- **The palette is lifted from the app's own** `:root` / `:root[data-theme="light"]`,
  so the page matches the thing it advertises. Vitta lets **sage** lead with gold as
  the money note, and the primary button follows the app's `--accent-fill` exactly:
  gold on dark, sage on light.
- **No hardcoded counts in headings** — the ladder may keep growing.
- **Single-codepoint emoji only.** ZWJ sequences render as tofu.

## A trap worth knowing

`body` uses `background-attachment: fixed`, which Chromium paints only for the
viewport. A stitched **`fullPage` screenshot therefore lies** — everything below the
fold comes out on white, faking a dark-mode contrast bug that does not exist. Verify
with scrolled viewport screenshots, or by probing computed styles.
