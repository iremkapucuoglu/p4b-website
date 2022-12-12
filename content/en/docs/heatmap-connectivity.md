---
title: Heatmap - Connectivity
permalink: "/docs/heatmap-connectivity/"
sections:
- technical
weight: 60
---

Different indicators serve as benchmarks for street connectivity and local accessibility for planning walking- and cycling-friendly neighborhoods. One of these indicators is a connectivity heatmap. The connectivity heatmap in GOAT allows the user to understand the degree of street network connectivity in the study area. This is especially important for promoting active modes (i.e. walking and cycling), as these modes are sensitive to detours.

<img src="\images\docs\technical_documentation\connectivity\connectivity_en_2.webp" alt="GOAT connectivity heatmap" style="max-height:380px;"/>


#### Calculation

The heatmap is computed using a hexagonal grid with an approximate edge length of 150 m per cell for walking mode (5 km/h). 

<img src="\images\docs\technical_documentation\connectivity\hexagonal_en.webp" alt="hexagonal" style="max-height:380px;"/>

Three isochrones (5, 10, and 15 min) are pre-computed using the centroid as a starting point for each grid cell. The size in m² of all three isochrones is summarized per cell:
<i>(average_reached_area = (isochrone1_area + isochrone2_area + isochrone3_area) / 3)</i>
and compared with all other cells using statistical quintiles. 

The grids are colored from high (green) to low connectivity (red). Changes in the street network are reflected by recomputing parts of the heatmap and updating the statistical classification. 




