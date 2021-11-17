+++
description = ""
sections = ["technical", ""]
title = "Heatmap - Connectivity"
translationKey = ""
weight = 65

+++
GOAT also includes another heatmap feature, called connectivity, which demonstrates the road network connections for the walkable environment. This heatmap feature can assist with addressing walkability, particularly in areas of low connectivity for which there may be lower chances for walking as an option.

![](/images/docs/technical_documentation/connectivity/connectivity.webp)

#### Calculation

Starting from the centroid of each hexagon, three isochrones are calculated (for 5 min, 10 min and 15 min). The average size of all three isochrones are taken and compared with the same value from all other grids. Using quintiles, the results are classified.

![](/images//docs/technical_documentation/connectivity/isochrone.webp)

![](/images//docs/technical_documentation/connectivity/legend_c.webp)