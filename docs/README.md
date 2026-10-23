# DaemonHall project site

Served by GitHub Pages from `main` → `/docs` at
<https://cybercoretech.github.io/DaemonHall/>.

- `index.html`: page content, plus `window.SITE` (default theme and the three signature mashups)
- `styles.css`: DaemonHall's own look (gothic hall, Halloween night); not the shared kit stylesheet
- `app.js`: the shared Cybercore project-site kit engine, unchanged (theme registry, 72 themes + mashups, copy buttons, reveal-on-scroll)
- `assets/`: the daemon mascot (full body + head) and favicon, original artwork

Themes load at runtime from the org site's registry (`/data/cybergrid.json`,
`/data/themes/<family>/<name>.json` on cybercoretech.github.io). A signature
mashup takes surfaces from its `base` palette and neons from its `accent`.

Local preview: serve a folder containing `DaemonHall/` (this dir) and `data/`
(copied or symlinked from the org site repo), then open
`http://127.0.0.1:<port>/DaemonHall/`.

The page consumes the versioned Cybercore Web Kit from
`https://cybercoretech.github.io/kit/v1/`. The shared theme runtime is no longer
copied into this repository; site-specific behavior remains in `index.html` and
`styles.css`. The runtime honors `window.SITE.web` motion/effect recipes and
`prefers-reduced-motion`.
