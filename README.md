# `imeantit`


---


## 🎨 Color Scheme Palette (24 Themes)

Each color uses a 4-letter identifier for the frame boundary/badge (`XXXX`) and appends a `b` for its matching light container background (`XXXXb`).

| Theme Group | Frame Tag (`#1`) | Background Tag | Suggested Usage |
| :--- | :---: | :---: | :--- |
| **Standard Core** | `blue` | `blueb` | Default edits / General tracking |
| | `orng` | `orngb` | High Priority Alerts / Data fixes |
| | `gren` | `grenb` | Reviewer 1 Responses |
| | `purp` | `purpb` | Reviewer 2 Responses |
| | `grey` | `greyb` | Typos / Minor grammar fixes |
| | `ylow` | `ylowb` | Reference / Bibliography updates |
| **Modern Tech** | `cyan`, `redx`, `pink`, `brow`, `lime`, `teal` | `...b` | Specialized domain or reviewer tracks |
| **Pastel Earth**| `sage`, `plum`, `rust`, `jade`, `gold`, `navy` | `...b` | Soft contrast layouts |
| **High Contrast**| `wine`, `clay`, `aqua`, `char`, `rose`, `sand` | `...b` | Deep accents / Subtle text offsets |

---

## 🛠️ Usage

### 1. The Block Container (`imeant` Environment)
Designed for multi-line edits, math, figures, lists, or large rewritten paragraphs.

#### Syntax Template:
```latex
\begin{imeant}[colframe=FRAME_COLOR, colback=BACKGROUND_COLOR]{Badge Title}{label:unique_key}
    Content space...
\end{imeant}
```

### 2. Micro-Edit Snippets (`\imeantinline` Command)
Designed to highlight mid-paragraph text modifications, tiny vocabulary updates, or localized mathematical symbols without breaking text wrapping or introducing ugly vertical spacing gaps. 

The first required argument acts as the label string inside a high-visibility, solid-colored tag badge.

#### Syntax Template:
```latex
\imeantinline[colframe=FRAME_COLOR, colback=BACKGROUND_COLOR]{Badge Tag Label}{label:unique_key}{Modified Inline Text}

### 3. Refer the highlight block label
using `\cref{}`
```latex
\cref{rev:baseline_clarity}
```
