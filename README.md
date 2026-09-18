# STEMonsters Interactives

Self-contained, single-file HTML interactives for Grades 3–12 STEM lessons, built by [STEMonsters Education](https://stemonsters.com). Hosted on GitHub Pages. There is no public gallery: each interactive is shared by its direct link.

## Layout

```
index.html                      blank landing page (nothing is listed here)
manifest.json                   private inventory: title, grade, topic, link for every interactive
interactives/
  <slug>/
    index.html                  one interactive, fully self-contained
```

Live URL pattern: `https://sonali-dasgupta.github.io/stem-interactives/interactives/<slug>/`

## Adding an interactive

1. Create a folder `interactives/<slug>/` — lowercase, hyphens, descriptive (`ohms-law-sim`). **Never rename a slug once it has been shared**; the URL is what students have.
2. Save the HTML as `index.html` inside it. Keep it single-file (inline CSS and JS, no external assets) so it works offline and never breaks.
3. Add an entry to `manifest.json`.
4. Commit and push. GitHub Pages redeploys in about a minute.

## Conventions

- One folder per interactive, one `index.html` per folder. Extra assets (images, data) go in the same folder.
- `visibility` in the manifest is `unlisted` (share by link) or `draft` (not yet ready to share). It is bookkeeping only; every file in the repo is reachable by URL.
- Keep the `<title>` meaningful — it is what students see in their browser tab and history.
- Tag a release (`git tag v2026-09`) when a batch is handed to a school so you know which version they have.

## Licence

© STEMonsters Education Pvt. Ltd. Shared with partner schools for classroom use.
