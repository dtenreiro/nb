# data

- `raw/` — source datasets, committed as-is when small (< ~10 MB). Never edit by hand.
- `processed/` — derived outputs. Git-ignored; regenerate from notebooks.

Larger files should go through Git LFS (`*.parquet`, `*.h5` are already configured in `.gitattributes`) or be downloaded by the notebook at runtime.

Notebooks load data via a path that works both locally and in Colab; see the `DATA_DIR` cell in `notebooks/00_template.ipynb`.
