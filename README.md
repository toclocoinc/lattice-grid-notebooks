# Lattice Grid notebooks

Runnable, keyless notebooks for [Lattice Grid](https://latticegrid.dev) in Jupyter, built on
[`lattice-grid-jupyter`](https://pypi.org/project/lattice-grid-jupyter/) (`pip install lattice-grid-jupyter`).
Each notebook lives in its own folder, installs with one `pip install` line, fetches real public data when it runs,
and works top to bottom on the free tier (no licence key) in Google Colab and JupyterLab.
Notebooks are committed with their outputs, so GitHub renders them.

| Notebook | What it shows | Data | Open |
|---|---|---|---|
| [`nyc-taxi-10m`](nyc-taxi-10m/nyc_taxi_10m.ipynb) | A 12.6-million-row dataframe in the large-dataframe mode: header histograms, filter to long airport trips, sort, `widget.selected` back as a pandas `DataFrame`, then pandas `groupby` and `pivot_table` | NYC TLC yellow-taxi trips, Jan-Apr 2024 (public Parquet) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/toclocoinc/lattice-grid-notebooks/blob/main/nyc-taxi-10m/nyc_taxi_10m.ipynb) |
| [`model-error-adult`](model-error-adult/model_error_adult.ipynb) | Where a gradient-boosted classifier goes wrong: a colour scale on the error, an actual x predicted pivot, grouping by sex / race / age band, a ROC chart bound to the grid that redraws for the segment you pick, and the wrong rows back as a pandas `DataFrame` | UCI Adult census income, CC BY 4.0 (fetched from the UCI archive) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/toclocoinc/lattice-grid-notebooks/blob/main/model-error-adult/model_error_adult.ipynb) |
| [`retail-forecast`](retail-forecast/retail_forecast.ipynb) | Forecast versus actual: an ETS forecast with 80% intervals fitted to monthly US retail sales, a grid of date / actual / forecast / lower / upper / residual with a diverging colour scale on the residual, a fan chart and an STL seasonal-decomposition chart bound to the grid that zoom to the period you pick, and the rows back as a pandas `DataFrame` | FRED RSXFSN (US Census Bureau, public domain; downloaded from FRED as CSV) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/toclocoinc/lattice-grid-notebooks/blob/main/retail-forecast/retail_forecast.ipynb) |

## Licence

The notebook code in this repository is MIT-licensed (see [`LICENSE`](LICENSE)). The `lattice-grid-jupyter` package it
installs is proprietary and is not part of this repository; it renders fully on `localhost` and in Colab's free/demo
mode without a key. Each notebook names the licence of the data it downloads.
