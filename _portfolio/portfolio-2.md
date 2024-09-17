---
title: "NDSAR, a multi-dimensional nonlocal speckle filter"
excerpt: "An efficient nonlocal filter to remove speckle from polarimetric, interferometric and multitemporal SAR data<br/><img src='/images/ndsar_preview.png' width='600'>"
collection: portfolio
---
The NDSAR filter comes in two versions:
- The NDSAR-BLF is a bilateral filter adapted to covariance matrices obtained from SLC multi-dimensional images. 
- The NDSAR-NLM is a generalization of the previous method which computes similarities on square patches instead of individual pixels. It is more robust to speckle than the bilateral but requires more computational power, depending on the user selected patch size.

I have released the open source Python/C++ implementations of the filters based which can be applied to any type of SAR data (Polarimetric, Tomographic, Inteferometric, Multi-temporal, PolInSAR).

Equivalent filters for single channel i.e. intensity images are also provided (special case of 1x1 covariance matrix).

Here is an example of an F-SAR image (DLR) filtered with NDSAR (left: original, right: filtered):  
<img src='/images/ndsar_preview.png' width='600'>

The figure below shows the impact of NDSAR on 3-D point cloud extraction from multi-baseline interferometric data (also called SAR tomography):  
<img src='/images/fig_NDSAR.png' width='400'>

Source code on [github](https://github.com/odhondt/ndsar)
