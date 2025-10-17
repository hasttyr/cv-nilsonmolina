# CV Nilson Molina (LaTeX)

Repositorio con las fuentes en LaTeX del currículum de Nilson Aldair Molina Rengifo (versiones en español e inglés). El propósito es mantener una fuente editable y reproducible para generar PDFs cuando sea necesario.

## Estructura

- `CV.NilsonMolina.tex` — Fuente en inglés.
- `CV.NilsonMolina.ES.tex` — Fuente en español.
- Archivos auxiliares generados por LaTeX (`*.aux`, `*.log`, `*.toc`, etc.).

## Requisitos

1. Una distribución de LaTeX instalada (MiKTeX o TeX Live).
2. `pdflatex` disponible en la variable PATH.
3. (Opcional) Editor recomendado: TeXstudio o VS Code con LaTeX Workshop.

## Cómo compilar (PowerShell)

Abre PowerShell en la carpeta del repositorio y ejecuta uno de los siguientes comandos según la versión que quieras generar:

```powershell
# Compilar la versión en inglés
pdflatex "CV.NilsonMolina.tex"

# Compilar la versión en español
pdflatex "CV.NilsonMolina.ES.tex"
```

Si el documento usa referencias internas o índices, ejecuta `pdflatex` dos veces. Si faltan paquetes, MiKTeX suele preguntar para instalarlos automáticamente.

## Limpiar archivos auxiliares (PowerShell)

Para eliminar archivos auxiliares generados por LaTeX:

```powershell
Remove-Item -Path "*.aux","*.log","*.toc","*.out" -ErrorAction SilentlyContinue
```
