# STEMonsters Interactives

Self-contained, single-file HTML interactives for Grades 3–12 STEM lessons, built by [STEMonsters Education](https://stemonsters.com). Hosted on GitHub Pages. There is no public gallery: each interactive is shared by its direct link.

## Layout

```
index.html                      landing page: logo + how-to-use (no list of interactives)
assets/image.png                STEMonsters logo, used by the landing page and every interactive header
manifest.json                   private inventory: title, grade, topic, link for every interactive
interactives/
  <slug>/
    index.html                  one interactive, fully self-contained
```

Live URL pattern: `https://sonali-dasgupta.github.io/stem-interactives/interactives/<slug>/`

## Adding an interactive

1. Create a folder `interactives/<slug>/` — lowercase, hyphens, descriptive (`ohms-law-sim`). **Never rename a slug once it has been shared**; the URL is what students have.
2. Save the HTML as `index.html` inside it. Keep CSS and JS inline; the only shared asset is the logo, referenced as `../../assets/image.png`.
3. Add the STEMonsters header block (copy the `.brand` div and its CSS from any existing interactive).
4. Add an entry to `manifest.json`.
5. Commit and push. GitHub Pages redeploys in about a minute.

## Conventions

- One folder per interactive, one `index.html` per folder. Extra assets (images, data) go in the same folder.
- `visibility` in the manifest is `unlisted` (share by link) or `draft` (not yet ready to share). It is bookkeeping only; every file in the repo is reachable by URL.
- Keep the `<title>` meaningful — it is what students see in their browser tab and history.
- Tag a release (`git tag v2026-09`) when a batch is handed to a school so you know which version they have.

## Licence

© STEMonsters Education Pvt. Ltd. Shared with partner schools for classroom use.
