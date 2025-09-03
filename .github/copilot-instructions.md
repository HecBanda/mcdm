# Copilot Instructions — Jupyter Notebooks

## Purpose
Use these rules when helping in Jupyter notebooks. Favor clear, short code that runs in cells and tells a story.

## General
- Write simple Python. Small, readable functions.
- Add brief comments only where they help.
- Prefer standard libs and common DS libs (numpy, pandas, matplotlib, seaborn, scikit-learn).
- Avoid heavy frameworks unless asked.
- Never hard-code file paths. Use `pathlib.Path` and project-relative paths.

## Notebooks (ipynb) specifics
- Assume VS Code Jupyter.
- Show code first, then a short explanation (1–3 lines).
- Keep each cell focused on one task.
- Avoid long outputs; truncate with `head()`, `.sample()`, or `.info()` summaries.
- When creating cells, group them in this order: **Imports → Config/Seed → Load Data → EDA → Feature Eng → Model → Evaluation → Save → Next Steps**.

## Reproducibility
- Set seeds when randomness is used.

## Prompts to follow

- If the user asks for “cell-by-cell”, generate code split into logical cells with short headings.
- If they ask for “single cell”, provide one cell that runs end-to-end.
- If unclear, default to cell-by-cell.

## Style

- PEP 8 for naming: snake_case for variables/functions.
- Type hints for new functions.
- F-strings for formatting.
- Raise clear ValueError/TypeError for invalid inputs.