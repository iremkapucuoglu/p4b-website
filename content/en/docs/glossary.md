---
title: Glossary   
permalink: "/docs/glossary/"
sections:
- glossary
weight: 10
---


#### Accessibility
Accessibility is defined first in 1959 as “the potential of opportunities for interaction”, which refers to the ease with which people or goods can reach a particular location ([Hansen, 1959](https://doi.org/10.1080/01944365908978307 "Visit Reference")). In the context of GIS and urban planning, it refers to the ease with which people can reach essential services, such as healthcare facilities, schools, or supermarkets. 

In general, accessibility is an important consideration in GIS and planning, as it can have a significant impact on the quality of life of residents in a particular area. By calculating and analyzing accessibility, planners can identify areas with accessibility shortcomings to essential services, either due to lack of opportunities or due lack of path connectivity, and develop measures to improve access for residents. 

#### Accessibility Instrument
An accessibility instrument is a tool used to calculate and analyze the accessibility of a particular location or region. It takes into account factors such as transportation options, distance, and travel time to determine how easily people can access essential services such as healthcare and education. This information is important for planners and policymakers to identify areas with low accessibility and develop strategies to improve them. 

#### Active Mobility
Active mobility refers to the use of human-powered modes of transport, such as walking, and cycling. It is an important part of sustainable transport as it reduces dependence on cars and helps to reduce carbon emissions. Active mobility also has many health benefits, such as reducing the risk of obesity and cardiovascular disease. 

<img src="/images/docs/technical_documentation/glossary/active_mobility_freepik.webp" alt="Active Mobility" style="max-height:500px;"/>  

_Image: [Designed by pch.vector / Freepik](http://www.freepik.com "Freepik")_

#### Area of Interest (AOI)
An Area of Interest (AOI) is a specific geographical region or boundary that is of particular interest or importance to a particular study or analysis. It can be a watershed, a forest, a park or any other geographic area relevant to the study. The AOI is usually defined by a set of coordinates or a polygonal boundary that encompasses the region of interest. 

#### Connectivity
Connectivity refers to the degree to which paths are connected to each other. The higher the path and intersection density, the higher the connectivity. The main obstacles to connectivity are, for example, rivers, railway lines, and highways.

Connectivity has a direct impact on accessibility, as it is decisive for the travel time to reach a certain destination. High connectivity is especially important for active modes, as these modes are particularly sensitive to detours. Thus, high connectivity is key to ensure accessibility to services and amenities and to promote sustainable mobility. 

#### H3 Grid <img src="/images/docs/technical_documentation/glossary/H3_grid_logo.webp" alt="h3_grid_logo" style="max-height:80px;"/>  
The H3 grid is a geospatial indexing system by Uber Technologies that partitions the Earth's surface into a hierarchical grid of hexagonal cells for more efficient and accurate representation and analysis of geospatial data. It uses a hexagonal tiling approach based on an icosahedron, creating a hierarchical structure with multiple levels of resolution. Key features include hierarchical indexing, compact and non-overlapping cells, global coverage, nearest neighbor analysis, and open source. The hexagonal shape allows for equidistant and consistent spatial representation, with different resolutions. The resolution 10 (approx. 75m edge length) is generally used for computing travel-times and resolution 9 (approx. 200m edge length) or higher is used for visualization. Values are aggregated from the higher to lower resolution by computing the mean used for computing and visualization in GOAT. 
<p align="center">
<img src="/images/docs/technical_documentation/glossary/H3_grid.webp" alt="h3_grid" style="max-height:500px;center"/>  

_Image: [Uber](https://eng.uber.com/h3/ "Uber H3 grid")_ 
<p>

#### Heatmap
A heatmap is a graphical visualization form that uses different colors to indicate the different values of a dataset. This allows for a quick understanding of the data presented. 

In GOAT, we, among others, use heatmaps to analyse the local accessibility (see [Heatmaps](/en/docs/heatmap/ "Indicator documenation on our heatmaps")) of different amenities, such as cafes, restaurants or supermarkets. The heatmap uses different colours to indicate the different accessibility values. This information can then be used to make decisions about aspects of planning. 

#### Indicator
An indicator is a mean to analyze a specific attribute or topic in a quantitative way. Usually, a standardised procedure is applied for this, e.g. by using a formula. In planning, indicators can be used to assess the current situation, to compare different locations with each other, as well as to monitor the progress towards specific goals or objectives, such as improving accessibility. 

#### Isochrone
An isochrone or catchment area is an indicator that shows how far people can travel in a given time with a given speed from a selected location. Isochrones can be calculated for any mode such as walking, cycling, car or public transport. Depending on the selected mode, the corresponding routing network is used.  

You can find further information on how we perform isochrone calculations in our [indicator documentation](/en/docs/isochrone/ "Isochrone documentation"). 


#### Land Use
Land use refers to the way that land is used and developed within a particular area. This can include residential, commercial, industrial, or natural uses, among others. Land use with associated population and POI density has a direct impact on accessibility opportunities.

Land use is therefore an important factor that should be assessed in an integrated way with transportation. For example, mixed-use development improves local accessibility and thus can reduce the need for car travel.

<p align="center">
<img src="/images/docs/technical_documentation/glossary/landuse.webp" alt="land-use" style="max-height:300px;"/>  

_Image: [Chatham House Sustainability Accelerator](https://accelerator.chathamhouse.org/article/land-use-challenges "Chatham House Sustainability Accelerator")_
<p>

#### Local Accessibility
Local accessibility, also known as neighborhood-level accessibility, refers to the ease with which people can access essential services within a specific neighborhood or area ([Handy, 1992](http://www.jstor.org/stable/23288518 "Visit Reference")). This type of accessibility usually refers to active modes and is typically measured using metrics such as the distance from a particular location to the nearest service, the number of services within a certain radius, or the travel time, which is used in GOAT, required to reach a service.  

#### Open Source <img src="/images/docs/technical_documentation/glossary/open_source.webp" alt="open_source" style="max-height:80px;"/>  
Open source refers to software or other products that are made available to the public with their source code freely accessible and modifiable. This allows individuals and organizations to modify and improve the product as needed, without restrictions on use or distribution. 

#### Planning Support System (PSS)
A planning support system is a digital tool used to support the planning and decision-making process for urban and regional development. It uses data and models to provide information on various aspects of planning, such as land use, transportation, and environmental impact. The tool allows planners to explore different scenarios and evaluate the potential outcomes of their decisions. 

#### Point of Interest (POI)
A point of interest (POI) is a specific location or point within a geographical area that is of particular interest or importance to a particular study or analysis. It can be a landmark, a building, an amenity or any other point that is relevant to the study. The POI is usually defined by a set of coordinates or a geographic identifier such as an address or a place name. 

In spatial analysis, the POI is used as a way of identifying and analysing data for a specific location. Therefore, POIs are also important for mapping and visualisation purposes, as they help to identify key locations and features within a geographical area. 

#### Quintile Classification
Quintile classification is a commonly used method in Geographic Information Systems (GIS) to divide data into equal groups based on their values. This method is useful for analyzing and visualizing patterns in data and can help identify trends and patterns that may not be obvious easily. 

In GIS, quintile classification is often used to create choropleth maps, which are maps that use color to represent different values of a variable. For example, a choropleth map of the population density of a city. The map would be divided into five color-coded categories, with each category representing a different range of population densities. 

The accessibility heatmaps in GOAT use quintile classification to determine what is high or low accessible. For the classification, we first assign all zero values which have “no accessibility” and then we sort the data from lowest to highest. We divide the data into 6 equal groups, each containing 20% of the total data. The values in each group are assigned a rank from 0 to 5, with 0 being the lowest (no accessibility) and 5 being the highest (very high accessibility). 

#### Regional Accessibility
Regional accessibility refers to the ease with which people can access essential services across a larger region, such as a city or a county (mostly for the motorized modes; public transport & car). Based on panel data from the national travel survey, regional accessibility is determined by calculating the total number of residents who need access to and from a specific location within generally accepted travel times, such as 30 minutes by car and 45 minutes by public transportation for home-to-work travel and occasional shopping trips ([Straatemeier, 2008](https://doi.org/10.1016/j.tranpol.2007.10.002 "Visit Reference")).  

#### Routing <img src="/images/docs/technical_documentation/glossary/routing_logo.webp" alt="open_source" style="max-height:80px;"/>  
Routing refers to the process of finding the best or most efficient path from one location to another. This is commonly used in transportation planning and navigation systems to help people get from point A to point B but also finds application in accessibility analysis to route from point A into all directions. 

#### Sustainability <img src="/images/docs/technical_documentation/glossary/sustainability.webp" alt="open_source" style="max-height:80px;"/>  
Sustainability refers to meeting the needs of the present without compromising the ability of future generations to meet their own needs. In the context of urban and regional development, sustainability involves balancing economic, social, and environmental factors to create livable and resilient communities. This includes reducing carbon emissions, promoting active mobility, and preserving natural resources. 

#### Transport Mode
Transport mode refers to the type of transportation used for a particular trip or journey. This can include modes such as transit (bus, train, subway), cycling (pedelec, bike), walking, and driving. The choice of transport mode can have a significant impact on factors such as travel time, cost, and environmental impact. 







### References
Hansen, W.G. (1959). How accessibility shapes land use. Journal of the American Institue of Planners. 25, 73–76.
https://doi.org/10.1080/01944365908978307 

Handy, S. L. (1992). Regional Versus Local Accessibility: Neo-Traditional Development and its Implications for Non-work Travel. Built Environment (1978-), 18(4), 253–267. http://www.jstor.org/stable/23288518 

Straatemeier, T. (2008). How to plan for regional accessibility?. Transport Policy, 15(2), 127-137. 
https://doi.org/10.1016/j.tranpol.2007.10.002 
