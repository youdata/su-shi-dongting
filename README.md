# 苏轼 · 洞庭春色赋 · 中山松醪赋

苏轼《洞庭春色赋》《中山松醪赋》合卷（吉林） — a narrated deep-zoom reading, as a static page (in Chinese).

Su Shi's two odes on wine in one scroll, with his own postscript of 1094 and the colophons: each of his 77 columns with its modern reading.

Live: https://youdata.github.io/su-shi-dongting/

The image pyramid is a tile folder (`dongting/`: `header.idx` + `{z}/{x}/{y}.png`), so any static host serves it.
Its fonts are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

## How it is made

From `infographic-examples/su-shi-dongting/build.mjs` (the page) with rx (`~/rx-cli`):

```sh
node build.mjs                                                     # → su-shi-dongting.json
rx export su-shi-dongting.json --out site --app /rx-graphic-editor/web/index.html --canvas --theme dark --lock-layers --tiles dir
rx publish site --to github:youdata/su-shi-dongting --yes
```
