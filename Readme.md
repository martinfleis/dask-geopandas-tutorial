# Dask-GeoPandas introduction tutorial

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/martinfleis/dask-geopandas-tutorial/main?urlpath=lab/)


## Setting up to follow the tutorial

### Step 1: download the tutorial material

If you are a git user, you can get the tutorial materials by cloning this repo:

```
git clone https://github.com/martinfleis/dask-geopandas-tutorial.git
cd dask-geopandas-tutorial
```

Otherwise, to download the repository to your local machine as a zip-file,
click the `download ZIP` on the repository page
<https://github.com/martinfleis/dask-geopandas-tutorial>
(green button "Code"). After the download, unzip on the location you prefer
within your user account (e.g. `My Documents`, not `C:\`).

### Step 2: install the required Python packages

To follow the tutorial, we recommend to create a `conda` environment to
ensure you have all the required packages installed (the
[environment.yml](environment.yml) file list the required packages).

If you do not yet have `conda` installed, you can install miniconda
(https://conda.io/miniconda.html) or the (larger) Anaconda distribution
(https://www.anaconda.com/download/).

Using conda, we recommend to create a new environment with all packages using
the following commands (after cloning or downloading this github repo and
navigating to the directory, see above):

```bash
# setting the configuation so all packages come from the conda-forge channel
conda config --add channels conda-forge
conda config --set channel_priority strict
# mamba provides a faster implementation of conda
conda install mamba
# creating the environment
mamba env create --file environment.yml
# activating the environment
conda activate geopandas-tutorial
```

In case you do not want to install everything and just want to try out the course material, use the environment setup by Binder [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/martinfleis/dask-geopandas-tutorial/main?urlpath=lab/) and open the notebooks rightaway.

### Step 3: starting Jupyter Lab

The tutorial itself is a [Jupyter notebook](http://jupyter.org/), an interactive  environment to write and run code.

In the terminal, navigate to the `dask-geopandas-tutorial` directory (downloaded or cloned in the previous section)

Ensure that the correct environment is activated.

```
conda activate geopandas-tutorial
```

Start a jupyter notebook server by typing

```
jupyter lab
```

---

Data included:

- `airports.csv` from <https://ourairports.com/data/>
- `world.parquet` as a copy of `naturalearth_lowres` dataset from geopandas
- `GADM` from GADM but that is not included in the repo due to the size
