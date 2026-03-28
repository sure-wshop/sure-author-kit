# SuRE Workshop @ IJCAI 2026 — Author Kit

[![Workshop Website](https://img.shields.io/badge/SuRE%20Workshop-Website-blue)](https://sure-wshop.github.io/)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey)](https://creativecommons.org/licenses/by/4.0/)

LaTeX author kit for the [**SuRE Workshop** @ IJCAI 2026](https://sure-wshop.github.io/).
Based on the official IJCAI 2026 style.

## Files

Download as zip: [![Download ZIP](https://img.shields.io/badge/Download-ZIP-green)](https://github.com/sure-wshop/sure-author-kit/archive/refs/heads/main.zip)

| File | Description |
|------|-------------|
| `sure26.tex` | Author template — start here |
| `sure26.sty` | Workshop style file |
| `sure26.bib` | Example bibliography |
| `named.bst` | BibTeX style (named citations) |
| `sure26.pdf` | Compiled example / formatting reference |

## Usage

Open `sure26.tex` and set the three workshop-specific options near the top:

```latex
% Track: long | short | position
\suretrack{long}

% Your submission number (assigned by the review system)
\suresubmissionnum{42}

% Uncomment for camera-ready; leave commented for submission
%\surecameraready
```

Then write your paper as usual. The track label appears automatically as a
running header (pages 2+) and as a footnote on page 1.

## Tracks and page limits

| Track | Content pages | Extra pages (refs / acks) |
|-------|:---:|:---:|
| `long` | 7 | +2 |
| `short` | 4 | +1 |
| `position` | 2 | +1 |

The content page limit is **strict** — papers exceeding it will be desk rejected.

## Submission vs. camera-ready

- **Submission** (default): header reads *Confidential SuRE Submission \<n\>: \<track\> paper*; line numbers are enabled.
- **Camera-ready**: add `\surecameraready` to the preamble and comment out `\linenumbers`; header reads *SuRE Workshop @ IJCAI 2026: \<track\> paper*.

## Compilation

```bash
pdflatex sure26
bibtex sure26
pdflatex sure26
pdflatex sure26
```
