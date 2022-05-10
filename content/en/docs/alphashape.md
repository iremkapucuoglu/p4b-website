---
title: Isochrone as Alphashape
permalink: /docs/alphashape/
sections:
- technical
weight: 40
---

GOAT allows you to calculate and visualize isochrones using alpha shapes. GOAT is using a very fast 2D concave hull algorithm, which is described in this paper  [A New Concave Hull Algorithm and Concaveness Measure for n-dimensional Datasets, 2012](https://journal.iis.sinica.edu.tw/paper/1/100295-3.pdf?cd=2217EEBB7C44EDA26) and is implemented in a Javascript library called [Concaveman](https://github.com/mapbox/concaveman). This library generates isochrones (polygons) representing the area from a set of points that can be reached in a dedicated time.

![](/images/docs/technical_documentation/alphashape/isochrone_as_alphashape.webp)

#### 1. Concave Hull
Concave hulls are often used to generalize bounding polygons around a given sets of points. Depending on the chosen concaveness the precision of the isochrone can differ. The following example illustrates the difference between a convex and a concave hull. 

##### 1.1. Points from the network

![](/images/docs/technical_documentation/alphashape/set_points.webp)

##### 1.2. Convex Hull 
Imagine you take an a rubber band and you stretch it around the points. This is called convex hull. As you can see this representation is missing level of detail but comes with the advantage of fast computation. 

![](/images/docs/technical_documentation/alphashape/convex_hull.webp)

##### 1.3. Concave Hull
A concave hull usually begins with a convex hull as the starting geometry and then tries to better fit the point dataset. Depending on the chosen concavity the shape can be more or less precise. Different parameters can also be used for the calculation of the isochrones, depending on the needed precision. However, rising precision comes with higher computation times. 

![](/images/docs/technical_documentation/alphashape/concave_hull.webp)

Therefore, GOAT uses a specific parameter for the calculation of the isochrones, that represents a compromise between accuracy and computation time. Thanks to the [PLV8 extension](https://github.com/plv8/plv8) the [Concaveman](https://github.com/mapbox/concaveman) library can be used directly in the PostgreSQL database.








