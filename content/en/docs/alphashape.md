---
title: Isochrones
permalink: /docs/alphashape/
sections:
- technical
weight: 40
---

#### Isochrone Definition

An isochrone or travel time map is an indicator that provides users with a clear visualization of how far they can travel in a given time from a selected location. Isochrones can be calculated from one or more starting points for modes such as walking, biking, driving, or public transport. Each mode includes input factors such as speed, infrastructure network, and travel time.

In GOAT, Isochrone shapes are dynamically created in the front end based on a travel time grid. Therefore, isochrone can be created fast and for different intervals on the fly, which allows to dynamically compute isochrone shapes and boundaries from the road network for each step in the front end.


#### Routing Modes

Depending on the chosen travel mode GOAT uses different parts of the street network. To keep the platform flexible the street network categories can be adjusted to the local study context when setting up the tool.

Depending on the availability of data in the study area and the planning purpose different routing profiles are available. These are walking, cycling, pedelec and public transport.


#### 1. Walking

Default routing profile for walking, considering all paths accessible by foot.

Default walking speed: 5km/h

<img src="\images\docs\technical_documentation\alphashape\walking_en.webp" alt="walking isochrone" style="max-height:85px;"/>

#### 2. Cycling

#### 2.1 Standard

Default routing profile for cycling, considering all paths accessible by bicycle.

Default cycling speed: 15km/h Depending on the surface, smoothness and slope of the different street segments, the cycling speed is adjusted accordingly.

<img src="\images\docs\technical_documentation\alphashape\standard_en.webp" alt="standard isochrone" style="max-height:88px;"/>

#### 2.2 Pedelec

Same as the standard routing profile, but with an increased cycling speed of 23 km/h.
For Pedelecs, slopes are considered with a lower impedance than for Standard bicycles.

<img src="\images\docs\technical_documentation\alphashape\pedelec_en.webp" alt="pedelec isochrone" style="max-height:80px;"/>


#### 3. Transit

In this routing mode users can compute intermodal accessibility centered around public transport.
As you can be seen in the figure users can adjust: 

-	The weekday (Monday to Sunday)
-	From Time - To Time 
-	Access Mode (How the user accesses the station, e.g., Walk, Bicycle),
-	Egress Mode (How the user exists the station e.g., Walk, Bicycle) 
-	Transit Modes (Tram,Rail,Bus or Rail).

<img src="\images\docs\technical_documentation\alphashape\transit_en.webp" alt="transit isochrone" style="max-height:300px;"/>


#### What planning questions can be answered?

-   How many points of interest can be reached by public transport within the time frame?
-   How many supermarkets can be reached from a certain point in a 10-minute walk?
-   How many people can access a public transport station within 5 minutes of cycling?
-   How many people can access a specific location within 20min by rail-based public transport (tram, underground, train)?

#### How does the calculation work? 
##### Routing algorithms- Walking and Cycling:

The routing for walking and cycling is based on a custom implementation of the widely used Dijkstra algorithm. In the implementation, the routing network is dynamically created and therefore allows the computation of scenarios. 

While the routing network is saved in the PostgreSQL/PostGIS database, the routing is done in Python using the just-in-time compiler Numba.

##### Routing algorithms- Public Transport:

Since public transport isochrone requires a combination of different data types it has more complexity than the other isochrone modes. (the region’s sidewalks, bikeways, scheduled public transport services…).

You can think this dataset is a collection of GTFS and OSM data through the R5 engine(Rapid Realistic Routing on Real-world and Reimagined networks) and intersection with the GOAT Database for the POI’s and population. We require this intersection since the R5 does not provide any information about the reached amenities, such as point of interest and population, the grid is intersected with the amenity data from the GOAT database. 

R5 is the routing engine for Conveyal, a web-based system that allows users to create transportation scenarios and evaluate them in terms of cumulative opportunities accessibility indicators. This figure on the below represents the grid interpolation with travel time cost from R5 engine:

<img src="\images\docs\technical_documentation\alphashape\r5_en.webp" alt="r5 isochrone" style="max-height:350px;"/>

As a result, the grid will include accessibility information for all the amenities for each minute of the travel-time window.

<img src="\images\docs\technical_documentation\alphashape\grid_en.webp" alt="r5 isochrone" style="max-height:150px;"/>

What we need to know about these grid cells, the resolution of the results depends on the Web Mercator zoom levels. Resolution is a trade-off between performance and accuracy. We require different zoom levels however walking and cycling have lower travel distances and therefore it is important to have the highest resolution possible. High zoom levels produce high-resolution results at the expense of computation time.

#### Visualization 

This is visualized by using "Marching square contour line algorithm", a computer graphics algorithm that can generate two-dimensional contour lines from a rectangular array of values.[1] 

This algorithm transforms the grid from a 2D array to a shape to visualize or analyzed.
An illustration of 2D image processing is shown in the figure. 

<img src="\images\docs\technical_documentation\alphashape\wiki.webp" alt="marching square" style="max-height:350px;"/>



If you want to reach more detailed content about isochrones and how they work, it can be accessed on the tutorial and video sections on the website.


#### References

[1]  J. F. de Queiroz Neto, E. M. d. Santos, and C. A. Vidal. “MSKDE - Using
Marching Squares to Quickly Make High Quality Crime Hotspot Maps”. en.
In: 2016 29th SIBGRAPI Conference on Graphics, Patterns and Images (SIBGRAPI).
Sao Paulo, Brazil: IEEE, Oct. 2016, pp. 305–312. isbn: 978-1-5090-3568-7. doi:
10.1109/SIBGRAPI.2016.049. url: https://ieeexplore.ieee.org/document/
7813048/

[2]  https://fr.wikipedia.org/wiki/Marching_squares#/media/Fichier:Marching_Squares_Isoline.svg

Majk Shkurti, "Spatio-temporal public transport accessibility analysis and benchmarking in an interactive WebGIS", Sep 2022. url: https://www.researchgate.net/publication/365790691_Spatio-temporal_public_transport_accessibility_analysis_and_benchmarking_in_an_interactive_WebGIS

Matthew Wigginton Conway,Andrew Byrd,Marco Van Der Linden. "Evidence-Based Transit and Land Use Sketch Planning Using Interactive Accessibility Methods on Combined Schedule and Headway-Based Networks", 2017. url: https://journals.sagepub.com/doi/10.3141/2653-06









