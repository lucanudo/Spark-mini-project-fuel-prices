# Big Data Processing with Spark project IT Tools 2 

This repository contains the notebook for the Spark Mini Project, focused on exploring and modeling French fuel price data (2022–2024).

## Contents
- `Spark_project _E&L.ipynb` — main notebook
- `config.yaml` — configuration file (paths and parameters)
- `data/*.csv.gz` — input datasets (mirrors the sources used by the notebook)
- `fr_departements.geojson` — France departments GeoJSON (for the choropleth maps)

> **Note on completeness:** the notebook is designed to be runnable end-to-end by downloading the required resources directly from the original sources.  
> The data files (`.csv.gz`), `config.yaml`, and the GeoJSON are included **for completeness and robustness**, so the project can still run even if external downloads fail or network access is limited.

The notebook will:
- load data (either from the original sources or from the local `data/` folder, depending on configuration),
- build weekly indices and a normalized `price_index`,
- generate trend plots and choropleth maps,
- run an exploratory EV proxy analysis (based on `Services2024`),
- train and evaluate a next-day forecasting baseline using Spark ML.

## Requirements
- Python 3.x
- Apache Spark / PySpark
- Common Python packages used in the notebook: `pyspark`, `pandas`, `matplotlib`, `folium`, `pyyaml` (and any other imports already present in the notebook)

## Reproducibility
- A “self-contained” GeoJSON loading step is included to ensure the choropleth map works even in a clean environment.
- Lightweight sanity checks validate `week_index` and `price_index` to catch pipeline issues early.


