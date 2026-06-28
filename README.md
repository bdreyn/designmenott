# Design Me Nott — Artist Portfolio

A modern, single-page portfolio site for a graphic designer / illustrator.
Daisy theme, white + pastel-yellow palette, built with Tailwind. No build step.

## Stack
- **HTML + Tailwind (Play CDN)** — everything lives in `index.html`, no compile step
- **Hosting** — GitHub Pages (static)

## Run locally
No Node/Python required. Just open `index.html` in a browser, or serve the
folder with any static server.

## How to customize

Everything you'll commonly change is marked with `EDIT ME` comments in `index.html`:

| What | Where |
|------|-------|
| Artist name / branding | Search `Design Me Nott` and the `<title>` / meta tags in `<head>` |
| Hero headline & intro | The `HERO` section |
| About text & stats | The `ABOUT` section |
| Services | The `SERVICES` section |
| Contact email & socials | The `CONTACT` section (email appears twice) |
| **Portfolio pieces** | The `pieces` array in the `<script>` near the bottom |

### Adding real artwork
1. Drop image files into an `images/` folder.
2. In the `pieces` array, set `img` to the path, e.g. `img: 'images/poster.jpg'`.
3. Leave `img: ''` to show a generated pastel daisy placeholder instead.

```js
const pieces = [
  { title: 'Sunflower Café — Brand identity', tag: 'Branding', img: 'images/cafe.jpg', h: 5 },
  // ...
];
```
`h` controls the placeholder tile height (for the masonry layout); it's ignored once you use a real image.

## Deploy to GitHub Pages
1. Push this folder to a GitHub repo.
2. Repo → **Settings → Pages → Source: Deploy from branch → `main` / root**.
3. Site goes live at `https://YOUR_USER.github.io/REPO_NAME/`.

> **Note:** This folder still contains a `CNAME` file pointing at `www.redlinerepairsllc.com`
> (leftover from a previous project) and unused `css/`, `js/`, `images/`, `favicon.svg`
> files. Delete the `CNAME` (or change it to the artist's real domain) before
> deploying, and remove the old `css/js/images` if you don't need them — the new
> site is fully self-contained in `index.html`.
