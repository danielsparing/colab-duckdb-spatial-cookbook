# Setting up your environment

![Supasit Chantranon via Unsplash](https://images.unsplash.com/photo-1580745168634-33c78f4c4177)

Colab actually comes with surprisingly many handy scientific computing and geospatial tools pre-installed, such as `numpy`/`pandas`, `geoopandas` or `duckdb`. Sometimes you just need a bit more.

The [Spatial Extension](https://duckdb.org/docs/stable/core_extensions/spatial/overview.html) of DuckDB is essential for this cookbook. Luckily it is extremely easy to install: [install_duckdb_spatial.ipynb](notebooks/install_duckdb_spatial.ipynb)

GDAL is one of those things. There are 4 ways covered here to install GDAL:
- GDAL option 1: Don't install GDAL! The Python `osgeo` package (which contains `gdal`, `ogr` etc.) is already installed.
- GDAL option 2: Don't install GDAL! Use the GDAL that already ships with DuckDB. [gdal_with_duckdb.ipynb](notebooks/gdal_with_duckdb.ipynb)
- GDAL option 3: Install with `apt-get`, this will give you the command line tooks like `ogr2ogr` but as of June 2025 you won't get Arrow or Parquet support. [install_gdal.ipynb](notebooks/install_gdal.ipynb)
- GDAL option 4: If you do need arrow and parquet, then install via `conda`, e.g. by using `miniforge`. [install_gdal_conda.ipynb](notebooks/install_gdal_conda.md)
