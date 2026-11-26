# CV — Nilson Aldair Molina Rengifo

Fuentes en LaTeX del CV (inglés y español) y de la carta de presentación, para generar los PDF de forma reproducible.

## Contenido

| Archivo | Descripción |
|---|---|
| `CV.NilsonMolina.tex` / `.pdf` | CV en inglés (versión principal) |
| `CV.NilsonMolina.ES.tex` / `.pdf` | CV en español |
| `cover-letter.tex` / `.pdf` | Carta de presentación en inglés |
| `plan.md` | Plan de actualización del CV |

Los archivos auxiliares de compilación (`*.aux`, `*.log`, `*.out`, …) están excluidos en `.gitignore`.

## Requisitos

Una distribución de LaTeX con `pdflatex`:

| Sistema | Instalación |
|---|---|
| Windows | `winget install MiKTeX.MiKTeX` |
| macOS | `brew install --cask mactex-no-gui` |
| Linux (Debian/Ubuntu) | `sudo apt install texlive-latex-extra texlive-fonts-recommended` |

Paquetes usados: `extsizes`, `lmodern`, `geometry`, `hyperref`, `enumitem`, `titlesec`.

Con MiKTeX, activa la instalación automática de paquetes faltantes:

```sh
initexmf --set-config-value "[MPM]AutoInstall=1"
```

Comprueba la instalación con `pdflatex --version` (reabre la terminal si no lo encuentra).

## Compilar

Desde la carpeta del repositorio. Cada CV se compila dos veces para que `hyperref` resuelva enlaces y marcadores.

```sh
pdflatex CV.NilsonMolina.tex
pdflatex CV.NilsonMolina.tex

pdflatex CV.NilsonMolina.ES.tex
pdflatex CV.NilsonMolina.ES.tex

pdflatex cover-letter.tex
```

## Convenciones

- Las versiones en inglés y español se mantienen en paridad: mismas secciones, viñetas y fechas.
- Cada CV ocupa como máximo 2 páginas.
- Al modificar un `.tex`, recompila y versiona también su `.pdf`.
