---
title: Data   
permalink: "/docs/data/"
sections:
- about
weight: 40
---

#### Data used in GOAT
Data is generally defined as a set of discrete values that describe quantity, quality, fact, statistic, or other fundamental units of meaning, or simply a set of symbols that can be further understood. Data is the basis for any calculation and is our most valuable asset. Therefore, GOAT uses different data sets from different sources, both spatial and non-spatial. The aim of Plan4Better is to provide accurate analysis based on high quality data at a reasonable cost. Thus, the challenge of processing geospatial data that is inconsistent from different sources is addressed by developing a diverse set of data integration, data disaggregation and data fusion workflows.


#### Data collection and data processing

The process of collecting and evaluating data from different sources is known as data collection. First, the data sets required for GOAT are identified, based on the assumption that not all data are equally important for all indicators. 
Second, the data collection method is defined according to the type of data set (spatial or non-spatial) with different data formats (e.g. shapefiles, GeoJSON). The datasets used to implement GOAT are updated at least once a year to provide up-to-date data. More frequent data updates are possible, for example for POIs. 
The datasets from our own collection and from public and proprietary sources used to improve the analysis in GOAT are shown in the figure and are further described below.

<img src="/images/docs/technical_documentation/data/en_cropped.webp" alt="data-sets" style="max-height:900px;"/>  

- **Points Of Interest:** We use a mix of different data sets including [OpenStreetMap (OSM)](https://wiki.openstreetmap.org/), data from open-geoportals or commercial sources. The best known, OSM, is a free, editable map of the whole world, built largely from scratch by volunteers and distributed under an Open Database License. Although the OSM dataset for Germany is generally quite good, the data is checked for completeness and accuracy, with Plan4Better also contributing to OSM itself.

- **Population and Buildings:** The population is disaggregated to the building level based on census data and district or municipality population counts, as well as various land use data. The processing is supported by 3D city models where available.

- **Public Transport Network:** For the public transport network and schedule, GTFS (General Transit Feed Specification) data is used to provide realistic and temporal dynamic travel time for public transport. 

- **Administrative Boundaries:** The data is used to delimit the boundary of a geographical area under the jurisdiction of some governmental or administrative entities, such as counties in Germany.

- **Street Network:** For walking and cycling, OSM is mainly used, but the road network data is flexible, so some other datasets are used as well. For cars, calibrated car routing networks from commercial providers are used to calculate travel times including network delays.

- **Additional Data:** There are a number of other datasets that allow users to connect geoportals and enhance the visualisation by choosing from different base maps. In addition, elevation models, street noise and accident point data sets are used to improve and vary the analysis carried out using GOAT. 

Data integration and data fusion steps are applied to combine the different data sets and are adapted to the local context. Moreover, further data processing steps (accuracy, completeness, reliability, relevance, and up-to-dateness) are also implemented to obtain an accurate and reliable data set.