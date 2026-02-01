# CV Nilson Molina (LaTeX)

Repositorio con las fuentes en LaTeX de documentos profesionales de Nilson Aldair Molina Rengifo. El propósito es mantener una fuente editable, versionada y reproducible para generar PDFs cuando sea necesario.

## Estructura

### Currículum Vitae
- `CV.NilsonMolina.tex` — CV en inglés (versión principal).
- `CV.NilsonMolina.ES.tex` — CV en español.

### Cartas de Presentación
- `cover-letter.tex` — Plantilla de carta de presentación en inglés.

### Archivos Generados
- `*.aux`, `*.bbl`, `*.blg`, `*.log`, `*.out` — Archivos auxiliares de compilación LaTeX.

## Requisitos

1. Una distribución de LaTeX instalada (MiKTeX o TeX Live).
2. `pdflatex` y `bibtex` disponibles en la variable PATH.
3. (Opcional) Editor recomendado: TeXstudio o VS Code con LaTeX Workshop.

## Cómo compilar (PowerShell)

Abre PowerShell en la carpeta del repositorio y ejecuta los siguientes comandos según el documento que quieras generar:

### Compilar CV en inglés
```powershell
pdflatex "CV.NilsonMolina.tex"
bibtex "CV.NilsonMolina"
pdflatex "CV.NilsonMolina.tex"
pdflatex "CV.NilsonMolina.tex"
```

### Compilar CV en español
```powershell
pdflatex "CV.NilsonMolina.ES.tex"
```

### Compilar carta de presentación
```powershell
pdflatex "cover-letter.tex"
```

> **Nota:** La doble compilación es necesaria para resolver referencias cruzadas y bibliografía correctamente. Si faltan paquetes, MiKTeX suele preguntar para instalarlos automáticamente.
