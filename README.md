# JSONBRUT

> **Brutalist JSON Power Visualizer & Suite** — Zero dependencies. One single HTML file. Visualizer, recursive diff engine, statistics dashboard, and inline editor.

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Dependencies](https://img.shields.io/badge/dependencies-zero-brightgreen)
![Single File](https://img.shields.io/badge/architecture-single--file-blue)

---

## Features

- **Auto View Detection** — Auto-renders Chat (Claude/ChatGPT exports), Table (CSV-like arrays), Tree, or Stats based on JSON structure.
- **Chat Transcript Tools** — In-conversation search with match stepping, conversation switcher, and long messages collapsed by default.
- **7 View Modes** — `AUTO`, `CHAT`, `TABLE`, `TREE`, `STATS`, `RAW`, and `DIFF`.
- **Recursive JSON Diff View** — Compare two JSON files side-by-side with additions/deletions highlighting.
- **Inline Editing** — Double-click primitive values in Tree view to modify and export updated JSON.
- **Statistics Dashboard** — Zero-dependency Canvas charts for data type distributions, missing data heatmaps, and numeric stats.
- **Command Palette (`Cmd+K`)** — Fuzzy command search & quick actions.
- **Multi-Format Export** — Export arrays to CSV, Markdown, YAML, or XML.
- **URL & Snapshot Sharing** — Load via API URL or share lightweight JSON via URL hash snapshots.
- **Privacy First** — 100% client-side parsing. Your data never leaves your browser.
- **Mobile-Native Shell** — Bottom tab bar, off-canvas drawer, bottom sheets, and card-based tables on phones.

---

## On Mobile

Phones get a different shell, not a shrunken desktop one:

| Desktop | Phone |
|---|---|
| View toggles in the topbar | Fixed **bottom tab bar** with all 7 views |
| Sidebar column | **Off-canvas drawer** — tap `☰`, swipe from the left edge, or swipe it away |
| Wide data grid | **Card layout** per row, with a sort picker (`▤ CARDS` / `▦ GRID` to switch) |
| `Cmd+K` command palette | `⌘` button opens the same commands as a **bottom sheet** |
| `alert()` confirmations | Non-blocking **toasts** + haptic feedback |
| Drag & drop two files to diff | **Tap either diff slot** to pick a file |
| Copy link to clipboard | Native **share sheet** via the Web Share API |
| `PREV` / `NEXT` paging | **Infinite scroll** with a `LOAD MORE` fallback |

### Gestures

| Gesture | Does |
|---|---|
| Swipe content left / right | Previous / next view |
| Swipe in from the left edge | Open entries, conversations, schema |
| Swipe the panel away | Close it (or tap outside) |
| Tap a value in `TREE` | Edit it inline |

They are introduced once on first run and stay documented under
**Gestures & Shortcuts** in the `⌘` command menu.

Also handled: notch and home-indicator safe areas, `100dvh` so the collapsing
browser bar never crops the layout, 16px inputs so iOS never zooms on focus,
retina-sharp charts, landscape re-layout, and `Add to Home Screen` for a
standalone, chrome-free launch.

---

## Large Files

Every render path is bounded, so a multi-MB export does not lock the browser:

- Table rows, raw lines, diff lines and chat messages all render in chunks and
  extend as you scroll.
- Schema inference samples arrays instead of walking every item.
- `EXPAND ALL` is capped per tap; filters and searches are debounced.
- Only the visible table representation is built — cards or grid, never both.

Measured on an iPhone 13 viewport with an **11.1 MB / 60k-row** file: load plus
first paint **214 ms**, ~1.7k DOM nodes on screen.

---

## Quick Start

```bash
# Clone repository
git clone https://github.com/saadibnainan/jsonbrut.git

# Open in browser — no server or build step needed
open jsonbrut/index.html        # macOS
xdg-open jsonbrut/index.html   # Linux
start jsonbrut/index.html       # Windows
```

---

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Cmd+K` / `Ctrl+K` | Open Command Palette |
| `1` - `4` | Quick-switch views (Auto, Chat, Table, Tree) |
| `d` | Toggle Dark / Light mode |
| `Esc` | Close active modal or Command Palette |
| `Double-Click` | Edit primitive value inline in Tree view (single **tap** on touch devices) |

---

## GitHub Pages Deployment

1. Go to **Settings → Pages** in your GitHub repository.
2. Under **Build and deployment**, set Source to `Deploy from a branch`.
3. Select `main` branch and `/ (root)`.
4. Click **Save**. Live URL: `https://saadibnainan.github.io/jsonbrut`

---

## License

[MIT License](LICENSE) © 2026
