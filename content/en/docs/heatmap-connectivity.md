---
title: Heatmap - Connectivity
permalink: "/docs/heatmap-connectivity/"
sections:
- technical
weight: 60
---

Different indicators serve as benchmarks for street connectivity and local accessibility for planning walking- and cycling-friendly neighborhoods. One of these indicators is a connectivity heatmap. The connectivity heatmap in GOAT allows the user to understand the degree of street network connectivity in the study area. This is especially important for promoting active modes (i.e. walking and cycling), as these modes are sensitive to detours.


#### Calculation

The heatmap is computed using a hexagonal grid with an approximate edge length of 150 m per cell for walking mode (5 km/h). 


<img src="\images\docs\technical_documentation\connectivity\hexagon_en.webp" 
alt="hexagonal" style="max-height:390px;"/>  

_Figure 1: Hexagonal grid as spatial unit for the heatmap_


Three isochrones (5, 10, and 15 min) are pre-computed using the centroid as a starting point for each grid cell. The size in m² of all three isochrones is summarized per cell ( average_reached_area = (isochrone1-area + isochrone2-area + isochrone3-area) / 3 ) and compared with all other cells using statistical quintiles. The average size of all three isochrones are taken and compared with the same value from all other grids. Using quintiles, the results are classified.


The grids are colored from high (green) to low connectivity (red). Changes in the street network are reflected by recomputing parts of the heatmap and updating the statistical classification. 


<img src="\images\docs\technical_documentation\connectivity\connectivity_en_2.webp" alt="GOAT connectivity heatmap" style="max-height:380px;"/>

_Figure 2: Heatmap of Connectivity Indicator in GOAT_











Three isochrones (5, 10, and 15 min) are pre-computed using the centroid as a starting point for each grid cell. The size in m² of all three isochrones is summarized per cell:
<i>(average_reached_area = (isochrone1_area + isochrone2_area + isochrone3_area) / 3)</i>
and compared with all other cells using statistical quintiles. 

The grids are colored from high (green) to low connectivity (red). Changes in the street network are reflected by recomputing parts of the heatmap and updating the statistical classification. 




