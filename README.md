# manasdedge08.github.io

Personal site, served by GitHub Pages from `main`.

`index.html` is the whole site: markup, styles and script in one file, no build
step and no external requests. At ~6 KB over the wire that is faster than
splitting it, since separate CSS and JS would each cost a round trip and the
stylesheet would block the first paint.

## Editing

Open `index.html` and edit it. To preview:

```bash
python3 -m http.server 8000
```

Push to `main` and Pages redeploys within a minute or so.

## Layout of the file

| Region | What lives there |
| --- | --- |
| `<head>` | metadata, Open Graph tags, JSON-LD, the pre-paint theme script |
| `<style>` | palette tokens, the twelve-column grid, one block per section |
| `<body>` | header, `#intro`, `#top`, `#work`, `#research`, `#about`, `#contact`, footer |
| `<script>` | theme toggle, the Pune clock, the scroll-reveal observer |

## Notes

- **No `CNAME` file.** One used to sit here pointing at `peoples-hhgoa.me`, which
  made every visit redirect to a host that no longer answers. If a custom domain
  is added later, point its DNS at Pages *before* committing the file.
- Theme follows the system setting until the visitor picks one, which is then
  remembered in `localStorage` under `portfolio-theme`.
- All motion is disabled under `prefers-reduced-motion`.
