<a href="https://colab.research.google.com/github/danielsparing/colab-duckdb-spatial-cookbook/blob/main/notebooks/install_gdal_conda.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

# Install GDAL command line tools in Colab with Parquet support

If we need Parquet support for e.g. [ogr2ogr](https://gdal.org/en/stable/programs/ogr2ogr.html) or other command-line GDAL tool, we can install the required packages via `conda`. Or to be more precise, via `conda-forge` and `miniforge`.

The `libgdal-arrow-parquet` extension package that we need is not available via `apt`, but [it can be installed](https://gdal.org/en/stable/download.html#conda) via conda-forge. So let's first install conda-forge [^1] (and update `$PATH` [^2]):

[^1]: The curl download link comes from [conda-forge](https://conda-forge.org/download) and their installation [instructions](https://github.com/conda-forge/miniforge?tab=readme-ov-file#install) on GitHub.

[^2]: the reason we edit environment variables in Colab in a Python cell, not in a shell cell, is so that it persists across different cells in the notebook.


```python
import os

!curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
!bash Miniforge3-$(uname)-$(uname -m).sh -b -p /usr/local/miniforge

os.environ["PATH"] = "/usr/local/miniforge/bin:" + os.environ["PATH"]

# if we don't set this environment variable, `ogr2ogr` will emit PROJ-related warnings
os.environ["PROJ_LIB"] = "/usr/local/miniforge/share/proj"
```

Now we can add arrow/parquet support:


```python
!conda install libgdal-arrow-parquet -q -y
```

And that's it:


```python
!ogr2ogr --formats | grep parquet
# Returns:
#   Parquet -vector- (rw+v): (Geo)Parquet (*.parquet)
```


```python

```
