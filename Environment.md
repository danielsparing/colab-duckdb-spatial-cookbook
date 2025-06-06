# Setting up your environment

![Supasit Chantranon via Unsplash](https://images.unsplash.com/photo-1580745168634-33c78f4c4177?q=80&w=960&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

Colab actually comes with surprisingly many handy scientific computing and geospatial tools pre-installed, such as `numpy`/`pandas`, `geoopandas` or `duckdb`. Sometimes you just need a bit more.

GDAL is one of those things. There are 3 ways covered here to install GDAL:
- GDAL option 1: Don't install GDAL! Use the GDAL that already ships with DuckDB. [gdal_with_duckdb.ipynb](gdal_with_duckdb.ipynb)
- GDAL option 2: Install with `apt-get`, this will give you most functionality but as of June 2025 you won't get Arrow or Parquet support.
- GDAL option 3: If you do need arrow and parquet, then install via `conda`, e.g. by using `miniforge`.
