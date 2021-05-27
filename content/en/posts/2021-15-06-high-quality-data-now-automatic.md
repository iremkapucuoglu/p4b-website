---
author: ramirez
categories:
- development
- data
date: 2021-05-15T13:00:00.000+00:00
description: ''
image: "/images/mapillary_banner.webp"
summary: The data quality is substitutionally increased by the new Mapillary API,
  which offers an automatic image segmentation and object detection. GOAT uses this
  high-quality data in its analysis of walkability and accessibility.
thumbnail: "/images/mapillary_thumbnail.webp"
title: High quality data, now automatic
translationKey: ''
draft: true
image: ""
summary: "One of the key challenges of building a planning instrument such as GOAT is the availability and the quality of the data used for the calculations. We are frequently searching new data sources, such as Mapillary."
thumbnail: ""
title: "High quality data, now automatic"
translationKey: ""

---
## The data challenge

One of the key challenges of building a planning instrument such as GOAT is the availability and the quality of the data used for the calculations. As you may remember, we have been using [Mapillary](https://www.mapillary.com/)’s services to tackle this problem. They have been doing an amazing work developing a platform to capture the cities in pictures and most importantly, extracting valuable data from the images.

Our story with Mapillary began in March 2020, when we completely mapped [Fürstenfeldbruck](https://www.open-accessibility.org/mapillary/ "Fürstenfeldbruck in Mapillary"), a town 10 km west of Munich. Since then, we have been using this tool to improve the data that is relevant to our analysis. Nevertheless, everything had been completely manual. We follow Mapillary’s Blog, and on 24 august 2020, they posted “[Mapillary map features now available globally in OpenStreetMap](https://blog.mapillary.com/update/2020/08/24/global-map-features-openstreetmap.html)”. After reading the updates, we didn’t wait to try out the new features. With this example, we would like to show how it had helped us.

## Mapillary plug-in for JOSM

This is an experience report of mapping and updating the pedestrian crossings in Fürstenfeldbruck. First, we got the base layer of crossings from [overpass-turbo.eu](https://www.overpass-turbo.eu). This layer includes all crossings mapped in [OpenStreetMap](https://www.openstreetmap.org/#map=5/50.151/9.539) (OSM), so the idea was to compare them with the crossings identified by Mapillary’s AI object detection algorithm.

For this analysis, we used [JOSM](https://josm.openstreetmap.de/). It is an OSM extensible editor for desktop, that allows very easily, and highly scalable, to edit features and attributes of the data. Now, Mapillary’s featurefacilitates to identify the traffic signals and their location within the JOSM interface.

Additionally, the street view feature helps to monitor the physical characteristics of the infrastructure and the accuracy of the location of the signs. In the case of a pedestrian crossing, we are especially interested in the type of infrastructure, such as a zebra crossing, or a refuge island in the middle. Accordingly, the tags of the existing infrastructure can be updated to match the images and the signs.![Same signs in different identifyed in different locations by Mapillary.](/images/mapillary_fig1.jpg "Mapillary locations")_Figure 1 Two sequences identifying the same signs in different locations_

However, sometimes different sequences can identify the same group of signs but locate them in completely different positions, as shown in Figure 1. Here, the blue sequence shows the signs located after the right turn (coming from the north-east) when, in fact, they are located before the turn. In this case, the green sequence located them in a more accurate position.

Mapillary’s sign identification algorithm was already available on their website, but now, having the plug-in in JOSM makes the tasks of identification and mapping much easier. It allows working at a larger scale and take advantage of the JOSM interface of layers that is more effective than the iD editor of OpenStreetMap. However, this process is still a visual inspection, and many details can be skipped. With an automated process, the quality of the information could improve dramatically.

## Mapillary API: image segmentation and object detection

Fortunately, soon after trying Mapillary’s updates on OSM, they released another feature on 28 August 2020, “[Global access to map data with the Mapillary API](https://blog.mapillary.com/update/2020/08/28/map-data-mapillary-api.html)”. It was the first step into the automation of data gathering.

Before telling you our work with Mapillary’s data, let’s have a small explanation of how the API works: It provides 3 ways to access its data: First, Images API, it returns the images from a spatial parameter (within a delimited square or a point with a radius); second, object detections API, it is a way to query by the content of the images; and Map Features API, that returns locations of objects as point features on the map extracted from multiple images.![Segmentation of Maxvorstadt in Mapillary](/images/mapillary_fig2.jpg "Maxvorstadt")_Figure 2 Segmentation of Maxvorstadt and Mapillary's algorithm_

One of our first uses of Mapillary’s API was to create a map of Maxvorstadt, Munich, by using different segments from the Object Detections API. In this case, we looked for images showing cars, the sky, vegetation, and sidewalks. Since Mapillary’s algorithm breaks the image into 65 classes of objects as shown in Figure 2, we extracted the images with the highest proportion of the classes of interest. Then, with a kernel network density estimation, we joined them to the streets.

As a result, as shown on the map Figure 2, it is also possible to identify streets with high vegetation, or dense parking offer. It is interesting to see how multiple streets have a high percentage of “sky”. This may be due to wide streets and large open spaces, such as around the Pinakothek, or simply because most cameras were pointing to the sky.

## Automation algorithm

Either way, we went even further! We did not want to analyze only one neighborhood in Munich. We wanted to capture the entire city, or even extend to other cities where GOAT is currently operating. Our first challenge was to call the API from larger areas.

To overcome it, we developed a function to break the area into a grid of smaller squares. The function also incorporates tiny time breaks in between the squares, so we would not overload the servers. Afterward, we join the extracted information from all the squares into a single .json file.

The second challenge was related to the parameter for the API. Depending on the data required, the API needs a different set of parameters that has to be changed manually. To solve it, we filtered our own library of objects from the complete list of the [Mapillary API Documentation](https://www.mapillary.com/developer/api-documentation/), this filtered library is within a yaml file, which has all the parameters required for the API.

Now, in a single run, the script can call multiple objects either from the Object detection API or the Map Features API. For a deeper understanding, we invite you to take a look into our work, in our [repo](https://github.com/goat-community/mapillary-api) in GitHub. Finally, the idea is to set these functions into a Lambda function on Amazon Web Services (AWS) with temporal and event triggers.

## Making use of the data

And how are we going to use this information? For accessibility and walkability analysis. Let’s say we are analyzing the walkability in a neighborhood at dark hours. With this kind of analysis, we are interested in factors that influence the decision to walk, since the context is “dark hour”, we may examine if people are doing a longer detour to avoid darker streets. In this case, our objects of interest would be light poles. The evaluation could be more accurate with this information.

Another example could be a city that wants to improve green space. They may want to execute a project to improve the urban landscape by implementing green facades. With the object detection feature, it is possible to identify which streets lack vegetation, to prioritize them in the project. These and many more applications are achievable by combining the high-quality data from Mapillary, with all the features that a planning instrument like GOAT can provide.