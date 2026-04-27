# Thesis_Paper_Latex
LaTeX thesis template for "A CNN-Based Intrusion Detection System for Imbalanced Network Traffic Data" — Dept. of CSE, Premier University Chattogram. Built with MiKTeX 24.1 &amp; VSCode. Includes full chapter structure, biblatex/biber setup, and a step-by-step local setup guide for Windows.


# 📄 CNN-Based Intrusion Detection System — Thesis LaTeX Template

> **A Convolutional Neural Network–Based Intrusion Detection System for Imbalanced Network Traffic Data**  
> Department of Computer Science & Engineering, Premier University Chattogram

This repository contains the complete LaTeX source of the above thesis paper. It is shared as a reusable template so juniors can adapt the structure for their own thesis projects.

---

## 🛠 Prerequisites

Install all three before proceeding:

| Tool | Version | Link |
|------|---------|------|
| MiKTeX | 24.1 x64 | https://miktex.org/download |
| VSCode | Latest | https://code.visualstudio.com |
| LaTeX Workshop (VSCode extension) | Latest | Search in VSCode Extensions panel |

---

## 🚀 Quick Start

1. **Download** this repository as a ZIP → click the green **Code** button → **Download ZIP**
2. **Extract** the ZIP to a path with no spaces, e.g. `C:\Users\YourName\Documents\thesis\`
3. **Open the folder** in VSCode: `File → Open Folder`
4. Open `main.tex` and press `Ctrl + S` — LaTeX Workshop compiles automatically

For the full step-by-step local setup guide (MiKTeX install, VSCode configuration, troubleshooting), see **[SETUP.md](SETUP.md)** or the HTML tutorial included in this repo.

---

## 📁 Project Structure

```
├── main.tex                    ← Entry point — compile this file
├── thesis.sty                  ← Formatting and style definitions
├── references.bib              ← Bibliography (BibTeX/biblatex)
├── title_page.tex
├── abstract.tex
├── dedication.tex
├── signature.tex
├── author_declaration.tex
├── chapters/
│   ├── introduction.tex
│   ├── literature_review.tex
│   ├── methodology.tex
│   ├── results.tex
│   ├── conclusion.tex
│   ├── literaturefolder/       ← Sub-sections for literature review
│   ├── methodologyfolder/      ← Sub-sections for methodology
│   ├── resultsfolder/          ← Sub-sections for results
│   └── commands/               ← Useful LaTeX snippet examples
└── Figures/
    ├── methodologyfigures/
    └── resultsfigures/
```

---

## ⚙️ VSCode Settings (Important)

This project uses **biblatex with biber** — not the older bibtex. Add this to your VSCode `settings.json` (`Ctrl+Shift+P` → *Open User Settings JSON*):

```json
{
  "latex-workshop.latex.tools": [
    {
      "name": "pdflatex",
      "command": "pdflatex",
      "args": ["-synctex=1", "-interaction=nonstopmode", "-file-line-error", "%DOC%"]
    },
    {
      "name": "biber",
      "command": "biber",
      "args": ["%DOCFILE%"]
    }
  ],
  "latex-workshop.latex.recipes": [
    {
      "name": "pdflatex → biber → pdflatex × 2",
      "tools": ["pdflatex", "biber", "pdflatex", "pdflatex"]
    }
  ],
  "latex-workshop.latex.autoBuild.run": "onSave",
  "latex-workshop.view.pdf.viewer": "tab"
}
```

---

## ✏️ How to Adapt for Your Own Thesis

- Edit `title_page.tex` — update your name, student ID, supervisor, and title
- Edit `main.tex` — update `\projectTitle`, `\firstAuthorName`, `\university`, etc.
- Write your chapters inside the `chapters/` folder
- Replace images in `Figures/` with your own
- Add your references to `references.bib`

---

## 🐛 Common Issues

| Problem | Fix |
|---------|-----|
| `pdflatex` not recognized | Add MiKTeX `bin\x64` folder to Windows PATH |
| Bibliography not showing | Run full recipe: `pdflatex → biber → pdflatex × 2` |
| `biber` not found | Open MiKTeX Console → Packages → search & install `biber` |
| Missing `.sty` package | Open MiKTeX Console → Packages → install the missing package |
| Figures not found | Make sure you opened the root folder (containing `main.tex`) in VSCode |

---

## 👥 Authors

- **Dhruba Dey** — Premier University Chattogram, CSE
- **Isfa Sultana Tarin** — Premier University Chattogram, CSE
- Supervised by **Kingshuk Dhar**, Assistant Professor, Dept. of CSE

---

## 📜 License

This template is shared for academic and educational use. Feel free to adapt it for your own thesis. Attribution appreciated but not required.
