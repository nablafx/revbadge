# `revbadge`
Multi-color highlight builder featuring block, inline, and word-level revision badges.

**Version:** `1.2.1`  
**Release Date:** `29/08/2026`  

---

The `revbadge` package provides an elegant, column-safe framework designed specifically for tracking major revisions and minor modifications in academic manuscripts. This package can also be used as a versatile document highlighting tool.

### Key Features
* **`revbadge` block environment:** Designed for long paragraphs, multi-line equations, lists, and rewritten sections.
* **`revbadgemultiline` block environment:** Shares the block feature set while permitting multi-line text inside the badge label itself.
* **`\wordbadge` macro:** A compact, self-contained on-line badge for quick metrics, tags, or word-level annotations without extended background track highlighting.
* **`\revbadgeinline` macro:** Executes tight, mid-sentence text corrections with soft-wrapping background highlight tracks without disrupting standard line spacing.

All components feature native, automated integration with `hyperref` and `cleveref` under a unified "highlight" reference counter, alongside a vibrant 24-theme color palette.

---

## Color Scheme Palette (24 Themes)

Each color uses a 4-letter identifier for the frame boundary/badge (`XXXX`) and appends a `b` for its matching light container background (`XXXXb`).

| Theme Group | Frame Tag (`#1`) | Background Tag | Suggested Usage |
| :--- | :---: | :---: | :--- |
| **Standard Core** | `blue` | `blueb` | Default edits / General tracking |
| - | `orng` | `orngb` | High Priority Alerts / Data fixes |
| - | `gren` | `grenb` | Reviewer 1 Responses |
| - | `purp` | `purpb` | Reviewer 2 Responses |
| - | `grey` | `greyb` | Typos / Minor grammar fixes |
| - | `ylow` | `ylowb` | Reference / Bibliography updates |
| **Modern Tech** | `cyan`, `redx`, `pink`, `brow`, `lime`, `teal` | `...b` | Specialized domain or reviewer tracks |
| **Pastel Earth**| `sage`, `plum`, `rust`, `jade`, `gold`, `navy` | `...b` | Soft contrast layouts |
| **High Contrast**| `wine`, `clay`, `aqua`, `char`, `rose`, `sand` | `...b` | Deep accents / Subtle text offsets |

---

## 🛠️ Usage

### 1. Block Containers (`revbadge` and `revbadgemultiline`)
Designed for multi-line edits, math, figures, lists, or large rewritten paragraphs.

#### Standard Block (`revbadge`)
```latex
\begin{revbadge}[colframe=FRAME_COLOR, colback=BACKGROUND_COLOR]{Badge Title}{label:unique_key}
    Content space...
\end{revbadge}
```
#### Multi-line Label Block (`revbadgemultiline`)
Use this when you need to write longer reviewer feedback or comments directly in the badge label:
```latex
\begin{revbadgemultiline}[colframe=FRAME_COLOR, colback=BACKGROUND_COLOR]{Detailed reviewer query text...}{label:unique_key}
    Content space...
\end{revbadgemultiline}
```

### 2. Compact Word Badges (`\wordbadge`)
Designed for tagging individual words, parameter updates, or standalone labels directly on the text line without extra background track highlighting.
```latex
\wordbadge[colframe=FRAME_COLOR, colback=BACKGROUND_COLOR]{Badge Tag}{label:unique_key}{Word or Phrase}
```

### 3.Micro-Edit Snippets (`\revbadgeinline`)
Designed to highlight mid-paragraph text modifications, vocabulary updates, or localized mathematical symbols with a continuous background highlight track while preserving paragraph wrapping.
```latex
\revbadgeinline[colframe=FRAME_COLOR, colback=BACKGROUND_COLOR]{Badge Tag}{label:unique_key}{Modified Inline Text}
```

### 4.Cross-Referencing Highlights (\cref) (`\revbadgeinline`)
