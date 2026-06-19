# clmt5405-final-project
Final project for Earth Data Science: analyzing NOAA OISST sea surface temperature change across major ocean regions.
# Sea Surface Temperature Change Across Major Ocean Regions

## Group Members

- Shiyi Xue, GitHub: sx2413-eloise
- Yijia Bai, GitHub: Amyinhox
- Hanchi Long, GitHub: hanchiiii

## Project Title

Sea Surface Temperature Change Across Major Ocean Regions Since the Satellite Era

## Research Question

How has sea surface temperature changed across major ocean regions since the satellite observation era?

## Dataset

We will use the NOAA Optimum Interpolated Sea Surface Temperature dataset from the LEAP Data Catalog:

https://catalog.leap.columbia.edu/feedstock/aws-noaa-optimum-interpolated-sst

The dataset is an analysis-ready Zarr dataset derived from NOAA OISST NetCDF files. It can be accessed directly in Python using Xarray:

```python
import xarray as xr

store = "https://ncsa.osn.xsede.org/Pangeo/pangeo-forge/noaa_oisst/v2.1-avhrr.zarr"
ds = xr.open_dataset(store, engine="zarr", chunks={})
```

The dataset includes daily sea surface temperature, sea surface temperature anomalies, sea ice concentration, and estimated error on a global 0.25-degree grid. The time period available in this Zarr store runs from 1981 to 2021.

## Analysis Summary

We will investigate how sea surface temperature has changed across major ocean regions during the satellite observation era. Using Xarray, we will compute spatial averages, annual means, anomalies, and simple warming trends for selected global and regional ocean areas. Our final notebooks will include maps, time series, anomaly plots, and regional comparisons to show where ocean surface warming has been strongest.

## Planned Division of Work

### Notebook 1: Global Sea Surface Temperature Change

This notebook will examine global SST patterns and long-term change. It will include global SST maps, a global mean SST time series, SST anomaly plots, and a simple map of warming trends.

### Notebook 2: Tropical Pacific and ENSO-Region Variability

This notebook will focus on the tropical Pacific, especially the Niño 3.4 region. It will analyze SST variability, SST anomalies, and how tropical Pacific variability compares with the global mean.

### Notebook 3: Comparison Across Major Ocean Basins

This notebook will compare SST changes across selected ocean basins, such as the Atlantic, Pacific, and Indian Oceans. It will include regional time series, anomaly comparisons, and a simple comparison of warming trends.

## Tools

We plan to use:

- Python
- Xarray
- NumPy
- Matplotlib
- Pandas, if needed
- Jupyter notebooks

## Repository Structure

```text
.
├── README.md
├── notebooks/
│   ├── global_sst_change.ipynb
│   ├── tropical_pacific_sst.ipynb
│   └── ocean_basin_comparison.ipynb
└── environment.yml
```
