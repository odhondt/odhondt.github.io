---
title: "EO-Tools, an open source Earth Observation software"
excerpt: "A pure python toolbox to search, download and process Sentinel-1 InSAR pairs, Sentinel-2 tiles and Digital Elevation Models.<br/><img src='/images/eo-tools-vignette.png' width='400'>"
collection: portfolio
---

<p float="left">
    <img src="https://raw.githubusercontent.com/odhondt/eo_tools/main/data/amp_vh_berlin.png" width="360">
    <img src="https://raw.githubusercontent.com/odhondt/eo_tools/main/data/coh_vh_berlin.png" width="360">
    <img src="https://raw.githubusercontent.com/odhondt/eo_tools/main/data/change_berlin.png" width="360">
    <img src="https://raw.githubusercontent.com/odhondt/eo_tools/main/data/s2_berlin.png" width="360">
</p>

EO-Tools is a python toolbox that does not rely any external software and takes advantage of modern geospatial & high performance computing modules like rasterio/gdal, geopandas, shapely, folium, xarray, dask and numba. 

Its goal is to ease the development of complex remote sensing processing chains combining different modalities like radar and optical. 

Currently, the implemented features are:
- Interferometric processing of Sentinel-1 pairs, including TOPS processing steps like azimuth deramping, DEM assisted coregistration, Range-Doppler terrain correction and Enhanced Spectral Diversity. Individual bursts can be processed as well as full products and cropped to any area of interest provided by the user.
- Amplitude geocoding of SLC Sentinel-1 images, with Beta or Sigma Nought calibration.
- Ability to apply processing in the SAR geometry and further project the results in a geographic coordinate systems using lookup-tables.
- Geocoding merging and cropping of Sentinel-2 products with selection of radiometric bands and optional color compositing (natural RGB, CIR, SWIR, etc)
- Easy exploration of Sentinel-1 footprints to retrieve interferometric pairs
- Downloading of various digital elevation models given a user defined  geometry
- Saving the results as COG (Cloud Optimized GeoTIFF) files
- Advanced interactive visualization functions on maps using a tile server (TiTiler)


More info, including tutorials in the docs: <a href="https://eo-tools.readthedocs.io/" target="_blank">eo-tools.readthedocs.io</a> 

Source code on [github](https://github.com/odhondt/eo_tools)

Conda-forge package: [![Conda Version](https://img.shields.io/conda/vn/conda-forge/eo-tools.svg)](https://anaconda.org/conda-forge/eo-tools)  


<!-- This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML.  -->
