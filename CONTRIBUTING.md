# contributing to chalk

thanks for wanting to improve chalk. this is a single-file project so the bar to contribute is low — no build tools, no package manager, no framework.

---

## ground rules

- keep it a single `.html` file — no bundlers, no npm, no frameworks
- keep it zero-dependency — no libraries pulled from cdns unless there is a very strong reason
- keep the gruvbox palette — do not introduce colors outside the defined css variables
- keep the input restrictions — they are intentional, not a bug
- test in at least chrome and firefox before submitting

---

## ways to contribute

- **bug reports** — use the bug report issue template
- **feature requests** — use the feature request issue template
- **code** — open a pr with a clear description of what and why
- **design** — if you have gruvbox-consistent ui improvements, show them

---

## development setup

no setup required.

```bash
git clone https://github.com/yourusername/chalk.git
cd chalk
open chalk.html   # or use a local server
```

to test with a local server:

```bash
python3 -m http.server 8080
# open http://localhost:8080/chalk.html
```

---

## pull request checklist

before submitting a pr, confirm:

- [ ] the app opens and works in a fresh browser tab
- [ ] localstorage saves and restores correctly after a refresh
- [ ] drag and drop still works
- [ ] shift+enter and ctrl+enter behave correctly
- [ ] word counts update live
- [ ] no new colors outside the gruvbox css variable set
- [ ] no external dependencies added
- [ ] the file is still a single self-contained `.html` file

---

## code style

the codebase is intentionally terse — css is minified-ish, js uses short variable names in hot paths. new contributions should match this style:

- 2-space indentation in js
- css properties on single lines where they fit
- no comments in css (they exist as `/* ── SECTION ── */` headers only)
- js functions are short and named clearly
- no classes, no modules — plain vanilla js

---

## reporting bugs

use the **bug report** issue template. include:

- browser and version
- os
- steps to reproduce
- what you expected vs what happened
- screenshot if relevant

---

## feature requests

use the **feature request** template. chalk is intentionally minimal — features that add complexity without clear benefit to the core use case (focused, distraction-free writing in cells) are likely to be declined.
