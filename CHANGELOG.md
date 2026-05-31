# changelog

all notable changes to chalk are documented here.
format loosely follows [keep a changelog](https://keepachangelog.com/en/1.0.0/).

---

## [1.0.0] — initial release

### added
- notebook-style cell layout with colab-inspired gutter and cell numbers
- gruvbox dark hard color scheme with 7 cycling accent colors
- pointer-event drag and drop with ghost card and drop indicator
- shift+enter to move to next cell (creates one if at end)
- ctrl+enter to insert new cell below current
- b key shortcut to add cell below active (when not in textarea)
- backspace on empty cell deletes it
- per-cell word count badge visible on hover
- total cell count and total word count in the bottom bar
- between-cell add zones on hover
- move up/down buttons in cell toolbar
- delete button in cell toolbar
- export to plain .txt file
- localstorage persistence under key `chalk-v2`
- input filtering — lowercase only, controlled symbol set
- silent uppercase-to-lowercase conversion
- paste filtering — strips disallowed characters on paste
- auto-resize textareas
- slide-in animation for new cells
- empty state hint
- clear all with confirmation
