# `revbadge`
Multi-color highlight builder featuring block and inline revision badges.

**Version:** `1.1`  
**Release Date:** `11/07/2026`  

---

The revbadge package provides an elegant, column-safe framework designed specifically for tracking major revisions and minor modifications in academic manuscripts.

The `revbadge` block environment for handling long paragraphs, multi-line equations, lists, and sections; `revbadgemultiline` shares the same propose but allow you to build multi-line badge label;  and the `\revbadgeinline` macro for executing tight, mid-sentence word corrections without disrupting standard line spacing. Both components feature a dynamic colored badge mechanism that labels modifications on the fly.

To simplify linking text revisions directly back to a peer-review response matrix or letter, the package provides native, automated integration with hyperref and cleveref under a unified "highlight" reference counter. Additionally, revbadge comes pre-packaged with a vibrant, 24-theme color palette accessible via highly memorable 4-letter macro color identifiers (e.g., blue, gren, orng, purp, ylow, grey).


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

### 1. The Block Container (`revbadge` Environment)
Designed for multi-line edits, math, figures, lists, or large rewritten paragraphs.

#### Syntax Template:
```latex
\begin{revbadge}[colframe=FRAME_COLOR, colback=BACKGROUND_COLOR]{Badge Title}{label:unique_key}
    Content space...
\end{revbadge}
```
### 2. Micro-Edit Snippets (`\revbadgeinline` Command)
Designed to highlight mid-paragraph text modifications, tiny vocabulary updates, or localized mathematical symbols without breaking text wrapping or introducing ugly vertical spacing gaps.

The first required argument acts as the label string inside a high-visibility, solid-colored tag badge.

#### Syntax Template:
```latex
\revbadgeinline[colframe=FRAME_COLOR, colback=BACKGROUND_COLOR]{Badge Tag Label}{label:unique_key}{Modified Inline Text}
```

### 3. Refer the highlight block label
using `\cref{}`
#### Syntax Template:
```latex
\cref{rev:baseline_clarity}
```
