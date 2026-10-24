# TOP 20 World Cup

A standalone, black-and-white, bilingual (EN/KO) browser tournament game for lists created in TOP 20.

## Features

- Loads the TOP 20 list from `localStorage['top20_studio_v1']` when hosted on the same origin (same scheme, hostname and port) as the original TOP 20 site.
- Manually imports an exported TOP 20 JSON file as an alternative.
- Requires 20 candidates (the numbering in the source list is not a ranking).
- Fully random tournament: 8 random candidates play 4 preliminaries, the remaining 12 get random byes, then 16 → 8 → 4 → 2 → champion. The 16 participants are reshuffled after the preliminaries.
- Saves the tournament in a separate key `top20_worldcup_v1` with undo, restart and replay.
- Language switch (EN/KO) and responsive design.
- No remote dependencies and no API key required.

## Deploy with GitHub Pages

Create a new public GitHub repository (e.g. `Top20-WorldCup`) under the **same GitHub account** as your `Top20` site. Upload `index.html`, `README.md`, `css/style.css`, and `js/app.js` preserving their paths. Go to **Settings → Pages → Deploy from a branch → main / (root)**.

Example public address: `https://chloenmax.github.io/Top20-WorldCup/`

When both websites are on `https://chloenmax.github.io` in the **same browser profile**, they share localStorage even though their paths differ. Different devices/browsers, private browsing or custom domains do **not** share the same localStorage. Use JSON import in those cases.

## Notes

- The site only **reads** the TOP 20 original key; it does not alter your saved TOP 20 list.
- The game saves locally and cannot sync across devices.
- `file://` local testing may isolate localStorage; GitHub Pages is recommended for automatic import testing.
- No JPG export is included in this initial World Cup version; the feature can be added later.
