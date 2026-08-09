# JSONBRUT

> **Brutalist JSON Power Visualizer & Suite** — Zero dependencies. One single HTML file. Visualizer, recursive diff engine, statistics dashboard, and inline editor.

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Dependencies](https://img.shields.io/badge/dependencies-zero-brightgreen)
![Single File](https://img.shields.io/badge/architecture-single--file-blue)

---

## Features

- **Auto View Detection** — Auto-renders Chat (Claude/ChatGPT exports), Table (CSV-like arrays), Tree, or Stats based on JSON structure.
- **7 View Modes** — `AUTO`, `CHAT`, `TABLE`, `TREE`, `STATS`, `RAW`, and `DIFF`.
- **Recursive JSON Diff View** — Compare two JSON files side-by-side with additions/deletions highlighting.
- **Inline Editing** — Double-click primitive values in Tree view to modify and export updated JSON.
- **Statistics Dashboard** — Zero-dependency Canvas charts for data type distributions, missing data heatmaps, and numeric stats.
- **Command Palette (`Cmd+K`)** — Fuzzy command search & quick actions.
- **Multi-Format Export** — Export arrays to CSV, Markdown, YAML, or XML.
- **URL & Snapshot Sharing** — Load via API URL or share lightweight JSON via URL hash snapshots.
- **Privacy First** — 100% client-side parsing. Your data never leaves your browser.

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
| `Double-Click` | Edit primitive value inline in Tree view |

---

## GitHub Pages Deployment

1. Go to **Settings → Pages** in your GitHub repository.
2. Under **Build and deployment**, set Source to `Deploy from a branch`.
3. Select `main` branch and `/ (root)`.
4. Click **Save**. Live URL: `https://saadibnainan.github.io/jsonbrut`

---

## License

[MIT License](LICENSE) © 2026
