# My CV

A professional CV/Resume built with LaTeX.

## Prerequisites

You need to have LaTeX installed on your system. The document uses `fontspec` package which requires XeLaTeX or LuaLaTeX.

### macOS

Install MacTeX (full TeX Live distribution):

```bash
brew install --cask mactex
```

Or install BasicTeX (smaller installation):

```bash
brew install --cask basictex
```

### Ubuntu/Debian

```bash
sudo apt-get install texlive-full
```

### Windows

Download and install [MiKTeX](https://miktex.org/download) or [TeX Live](https://www.tug.org/texlive/windows.html).

## Project Structure

```
mycv/
├── README.md
├── mycv.iml
└── src/
    └── main.tex
```

## How to Compile

Navigate to the `src` directory and compile using `xelatex`:

```bash
cd src && xelatex main.tex
```

**Note:** XeLaTeX is required because the document uses the `fontspec` package with custom fonts (Arial).

### Full compilation (with bibliography)

If you have citations, run:

```bash
cd src && xelatex main.tex && biber main && xelatex main.tex && xelatex main.tex
```

## View the PDF

### macOS

```bash
open src/main.pdf
```

### Linux

```bash
xdg-open src/main.pdf
```

### Windows

```bash
start src/main.pdf
```

## Customization

- Edit `src/main.tex` to update your CV content
- The document uses Arial font by default (set via `\setmainfont{Arial}`)
- Colors can be customized by modifying the hex values in `\color[HTML]{...}`

## Troubleshooting

### Font not found

If you get a font error, make sure Arial is installed on your system, or change `\setmainfont{Arial}` to another available font.

### Package not found

Install missing packages using your TeX distribution's package manager:

- **MacTeX/TeX Live:** `tlmgr install <package-name>`
- **MiKTeX:** Use the MiKTeX Console to install packages

## License

This CV template is for personal use.

