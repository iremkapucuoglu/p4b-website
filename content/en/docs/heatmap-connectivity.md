---
title: Heatmap - Connectivity
permalink: "/docs/heatmap-connectivity/"
sections:
- technical
weight: 60
---

GOAT provides a heatmap that shows the area connectivity, which demonstrates how well the road network is connected. This is especially important for promoting active modes (i.e. walking and cycling), as these modes are sensitive to detours. A hexagonal grid is used for visualization.

![GOAT connectivity heatmap](/images/docs/technical_documentation/connectivity/connectivity_en.webp "GOAT connectivity heatmap")

#### Calculation

Starting from the centroid of each hexagon, three isochrones are calculated (for 5 min, 10 min and 15 min). The average size of all three isochrones are taken and compared with the same value from all other grids. Using quintiles, the results are classified.

![Calculation methodology](/images//docs/technical_documentation/connectivity/isochrone_en.webp "Calculation methodology")

