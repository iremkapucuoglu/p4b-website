---
author : "meining"
categories : ["use cases"]
date : 2023-04-17T09:00:00Z
description : "GOAT is a versatile planning tool that can be used in location planning, among other things. In this blog post we give a closer look at the use of GOAT in urban development concepts."
draft : false
image : "/images/blog/use-cases-development-concepts/stadtplanung_900450.webp"
summary : "GOAT is a versatile planning tool that can be used in location planning, among other things. In this blog post we give a closer look at the use of GOAT in urban development concepts."
thumbnail : "/images/blog/use-cases-development-concepts/stadtplanung_600450.webp"
title : "GOAT Use Cases: urban development concepts"
translationKey : "use-cases-development-concepts"
---
## What is an urban development concept?

An urban development concept seeks to support and develop the characteristics of a city in a future-oriented, sustainable and long-term manner. Interdisciplinary and cross-disciplinary communication as well as the inclusion of current trends is essential (complan Kommunalberatung GmbH, 2017). Currently, both the "15-minute-city" and an expansion of local mobility and alternative forms of mobility such as car and bike sharing are of great importance in many cases (complan Kommunalberatung GmbH, 2017). This is intended to strengthen urban and local supply centers.

## How can GOAT contribute to this?

### Visualization of spatial data

[GOAT](/../en/goat/ "What is GOAT?") is a WebGIS and contains a variety of spatial data. For example, buildings, population densities, land uses, points-of-interest (POIs), district boundaries, noise pollution, and much more information can be overlaid (see Figure 1).

![GOAT: Landuse Freiburg](/images/blog/use-cases-development-concepts/abb1-en.webp "GOAT: Landuse Freiburg")

_Figure 1: Representation of the land use map in GOAT._

### Connectivity and quality of the path network

For pedestrian and bicycle traffic, good connectivity between urban neighborhoods is essential. In GOAT, the existing path network can be visualized for the different modes of transport. With the help of the [connectivity heatmap](/en/docs/heatmap-connectivity/ "documentation on the connectivity heatmap"), it is possible to analyze how well the networks for pedestrian and bicycle paths are interconnected and thus identify potential for improvement. Scenario creation can also be used to analyze the impact of new path connections (e.g., a new bicycle bridge) on accessibility.

Since not only the availability of paths but also the attractiveness of the paths is crucial, further information such as surface conditions of the paths, gradients and accident statistics are integrated. For an overall analysis of the cycling offer, further infrastructural elements, such as bicycle parking facilities and bicycle repair stations, can also be integrated into GOAT.

If locally available, data on the freedom-of-barriers of footpaths can also be stored in GOAT and thus used for planning inclusive public spaces.

### Accessibility analysis

In order to achieve the goal of decentralized services of public interest, a fair distribution of important facilities for daily needs across the urban area is essential. To determine whether all citizens can reach all important facilities within a reasonable time (ideally with sustainable modes), accessibility analyses are a suitable method.

Our open source planning software GOAT contains various POIs like sports facilities, supermarkets, kindergartens and parks. These can be visualized and their spatial distribution analyzed with different accessibility indicators and intersected with population data. [Isochrones](/en/tutorials/isochrone/ "tutorial on isochrones") and [heatmaps](/en/docs/heatmap/ "documentation about the local accessibility heatmap") can be used to find gaps in accessibility, identify opportunities for redensification, and thus address shortcomings.

A good benchmark for accessibility are the results of [multi-isochrones](/en/tutorials/multiisochrones/ "tutorial on multi-isochrones"). This form of isochrones calculate which proportion of residents inside a neighborhood has access to a particular amenity (e.g. supermarket, kindergarten). Different means of transport as well as travel time can be chosen. Figure 2 shows an exemplary accessibility analysis with isochrones to supermarkets within 10 minutes.

![GOAT: Accessibility to supermarkets](/images/blog/use-cases-development-concepts/abb2-en.webp "GOAT: Accessibility to supermarkets")

_Figure 2: Multi-isochrones showing accessibility to supermarkets in GOAT._

### Scenarios for location planning

The enhancement and strengthening of pedestrian-friendly urban and local supply centers is considered an important point in the planning of urban development concepts (complan Kommunalberatung GmbH, 2017, p. 43). With GOAT, in addition to analyzing the current state, interactive scenarios can be created for [new POIs](/en/tutorials/scenario-location/ "Learn how to add new POIs in GOAT"), [path connections](/en/tutorials/scenario-ways/ "Learn how to modify paths in GOAT") and [buildings](/en/tutorials/scenario-buildings/ "Learn how to create building scenarios in GOAT") and their impact on accessibility can be analyzed. In this video, we show how scenarios can be analyzed in GOAT.

<iframe class="embed-responsive-item" src="https://player.vimeo.com/video/754586552?h=ebea094923" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen data-uk-responsive width="1920" height="1080"></iframe>

Furthermore, locations of alternative and sustainable mobility such as carsharing, bikesharing or charging stations for e-cars can be displayed and dynamically edited or additional stations can be added. Thus, ideal new locations can be identified to provide access to these environmentally friendly mobility options to the entire population in the future, if possible.

## Try GOAT!

Do you also want to perform location planning analyses with GOAT or are you interested in further information? [Contact us](/en/contact/ "Contact Plan4Better here!") or try the [free GOAT demo](/en/request-demo/ "Try GOAT for free!")!

## References

complan Kommunalberatung GmbH, 2017. Stadt Jena. 2030+ - Integriertes Stadtentwicklungskonzept. Stadt Jena, Jena.