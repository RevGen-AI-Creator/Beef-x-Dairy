# Beef-x-Dairy

Beef on Dairy Calculator — data analysis and calculations for beef-on-dairy cattle.

## Project layout

```
beef-x-dairy/
├── data/
│   ├── raw/            # Original, untouched source data (not committed)
│   └── processed/      # Cleaned / transformed data (not committed)
├── notebooks/          # Jupyter notebooks for exploration
├── outputs/            # Charts, reports and exported results (not committed)
├── src/beef_x_dairy/   # Reusable Python code: calculations, data loading
├── tests/              # Tests for the calculations
├── requirements.txt    # Python dependencies
└── pyproject.toml      # Package configuration
```

## Getting started

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
pip install -e .
pytest
```

## Working conventions

- Put source data files in `data/raw/` and never edit them by hand; write
  cleaned versions to `data/processed/`.
- Keep calculation logic in `src/beef_x_dairy/` so notebooks and scripts
  share the same, tested formulas.
- Add a test in `tests/` for each new calculation.
