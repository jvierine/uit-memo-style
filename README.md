# UiT Memo Style

Reusable LaTeX package extracted from the MM memo-series `mmmemo.sty`.
This repository is private; no compiled memo documents belong here.
The UiT seal is institutional branding, not a grant of trademark rights or endorsement.

Copy `uitmemo.sty` and `assets/uit-circular-logo.pdf` into an Overleaf project,
or pin this repository as a Git submodule. Keep the source revision in the
consuming project's provenance. No TeX shell escape is required.

```latex
\documentclass[11pt]{article}
\usepackage{uitmemo}
\renewcommand{\uitseries}{HEIMDALL GNSS PROCESSING MEMO SERIES}
\renewcommand{\uitprefix}{HEIMDALL}
\begin{document}
\uitmemo{21}{2026-09-14}{HEIMDALL team}{Juha Vierinen}{A specific question}
\makeuitmemo
Memo text.
\end{document}
```

`\scriptprovenance{analysis/script.py}` is visible by default.
Use `\hidescriptprovenance` to hide it. Override `\uitlogo` for a relocated seal.
The existing MM checkout is deliberately not modified by extracting this package.
