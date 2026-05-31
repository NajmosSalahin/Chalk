# chalk

> a notebook for your brain. gruvbox-dark, zero friction, no server.

chalk is a minimal notebook app inspired by jupyter/colab — built as a single self-contained HTML file. write in cells, reorder them, think in blocks. everything saves to your browser automatically.

---

## features

- **notebook-style cells** — add, delete, reorder freely
- **pointer drag & drop** — drag the handle to reorder; works on touch too
- **gruvbox dark theme** — full palette, cycling accent colors per cell
- **per-cell word count** — visible on hover
- **total word + cell count** — live in the bottom bar
- **export** — dumps all cells to a plain `.txt` file
- **zero server** — one `.html` file, runs offline, no build step
- **localStorage persistence** — survives refreshes and tab closes
- **input enforcement** — lowercase only, controlled symbol set; no accidental caps or stray punctuation

---

## keyboard shortcuts

| shortcut | action |
|---|---|
| `shift` + `enter` | move to next cell (creates one if last) |
| `ctrl` + `enter` | create new cell below current |
| `b` (outside textarea) | create new cell below active |
| `backspace` on empty cell | delete that cell |
| `↑` / `↓` buttons | move cell up or down |

---

## allowed characters

chalk enforces a minimal character set by design — it's a thinking tool, not a text editor.

**allowed:** `a–z` · `0–9` · spaces · newlines · `+ - * / = < > % ^ ( ) [ ] { } . , ' ?`

**auto-converted:** uppercase letters → silently lowercased

**blocked:** `! @ # $ & | \ ; : " `` ~ _` and all other symbols

---

## usage

### option 1 — open directly

```
open chalk.html
```

works in any modern browser. no install, no dependencies, no internet required after the first load (fonts are fetched from Google Fonts on first open).

### option 2 — serve locally

```bash
# python
python3 -m http.server 8080

# node
npx serve .

# then open http://localhost:8080/chalk.html
```

### option 3 — deploy to github pages

1. fork this repo
2. go to **Settings → Pages**
3. set source to `main` branch, root `/`
4. your chalk instance will be live at `https://yourusername.github.io/chalk/chalk.html`

---

## data & privacy

- all data is stored in `localStorage` under the key `chalk-v2`
- nothing is ever sent anywhere
- clearing browser storage clears your notes — export first if needed
- incognito/private windows do not persist data

---

## stack

| what | detail |
|---|---|
| runtime | vanilla js, no frameworks |
| fonts | JetBrains Mono + Syne via Google Fonts |
| theme | [gruvbox](https://github.com/morhetz/gruvbox) dark hard |
| storage | browser `localStorage` |
| drag & drop | pointer events api (no html5 drag api) |
| build | none |
| dependencies | none |

---

## file structure

```
chalk/
├── chalk.html          # the entire app — html + css + js in one file
├── README.md           # this file
├── CHANGELOG.md        # version history
├── CONTRIBUTING.md     # how to contribute
├── LICENSE             # mit license
└── .github/
    ├── ISSUE_TEMPLATE/
    │   ├── bug_report.md
    │   └── feature_request.md
    └── workflows/
        └── deploy.yml  # github pages auto-deploy
```

---

## contributing

see [CONTRIBUTING.md](./CONTRIBUTING.md).

---

## license

[MIT](./LICENSE) — do whatever you want with it.

---

## acknowledgements

- [gruvbox](https://github.com/morhetz/gruvbox) by morhetz — the color scheme this entire project is built around
- [JetBrains Mono](https://www.jetbrains.com/lp/mono/) — the typeface
- [Syne](https://fonts.google.com/specimen/Syne) — used for the logo
