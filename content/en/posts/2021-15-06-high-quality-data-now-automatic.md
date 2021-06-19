---
author: ramirez
categories:
- development
- data
date: 2021-05-15T13:00:00.000+00:00
description: ''
image: "/images/blog/high_data_quality/mapillary_banner.webp"
summary: The Mapillary API is the first step towards automating data collection through automated image recognition and image segmentation. We use this data in GOAT to improve the data basis of our analyses.
thumbnail: "/images/mapillary_thumbnail.webp"
title: High quality data, now automatic
translationKey: ''
draft: false

---
## The data challenge

One of the key challenges of building a planning instrument such as GOAT is the availability and the quality of the data used for the calculations. As you may know, one of the data sources we use to solve this problem is [Mapillary](https://www.mapillary.com/). 

Mapillary is a platform through which image sequences of the street scape can be captured and shared with the open community. From these images, valuable data can be extracted. 

Our story with Mapillary began in March 2020, [when we completely mapped Fürstenfeldbruck](https://www.open-accessibility.org/mapillary/ "Fürstenfeldbruck in Mapillary"), a town 10 km west of Munich. Since then, we have been using the image sequences collected from us and other users to improve the data that is relevant for our analyses. Until now, all the steps (analysis of the images, object detection, saving the gained information, etc.) were done completely manually.

We follow Mapillary’s Blog, and on 24 august 2020, they posted “[Mapillary map features now available globally in OpenStreetMap](https://blog.mapillary.com/update/2020/08/24/global-map-features-openstreetmap.html)”. After reading the updates, we didn’t wait to try out the new features. With the following example, we would like to show how it had helped us.

## Mapillary plug-in for JOSM

This is an experience report of mapping and updating the pedestrian crossings in Fürstenfeldbruck. First, we got the base layer of crossings from [overpass-turbo](https://www.overpass-turbo.eu). This layer included all crossings mapped in [OpenStreetMap](https://www.openstreetmap.org/#map=5/50.151/9.539) (OSM), so the idea was to compare them with the crossings identified by Mapillary’s AI object detection algorithm.

For this analysis, we used [JOSM](https://josm.openstreetmap.de/). It is an extensible OSM editor for desktop, that allows very easily, and highly scalable, to edit features and attributes of the data. Via the [Mapillary-Plugin](https://help.mapillary.com/hc/en-us/articles/115001739989-Mapillary-JOSM-plugin) it is now possible to display the crosswalks and their location detected from the Mapillary images in JOSM.

In addition, the street view feature helps to verify the physical attributes of the infrastructure and the accuracy of the position of objects (e.g., traffic signs, lane markings). In the case of a crosswalk, we are particularly interested in attributes such as freedom-of-barriers and the type of crossing (traffic light, crosswalk, refugee island, etc.). This information can be derived from the images and accordingly the OSM tags of the existing infrastructure can be enriched.

![Same signs in different identified in different locations by Mapillary.](/images/blog/high_data_quality/mapillary_fig1.webp "Mapillary locations")_Figure 1 Two sequences identifying the same signs in different locations_

However, sometimes different image sequences can identify the same traffic sign but locate it in completely different positions, as shown in Figure 1. Here, the blue sequence shows the signs located after the right turn (coming from the north-east) when, in fact, they are located before the turn. In this case, the green sequence located them in a more accurate position.

Mapillary’s sign identification algorithm was already available on their website, but now, having the plug-in in JOSM makes the tasks of identification and mapping much easier. It allows working at a larger scale and take advantage of the JOSM interface of layers that is more effective than the iD editor of OpenStreetMap. However, this process is still a visual inspection, and many details can be skipped. With an automated process, the quality of the information could improve dramatically.

## Mapillary API: image segmentation and object detection

Fortunately, soon after trying Mapillary’s updates on OSM, they released another feature on 28 August 2020, “[Global access to map data with the Mapillary API](https://blog.mapillary.com/update/2020/08/28/map-data-mapillary-api.html)”. It was the first step into the automation of data gathering.

Before telling you our work with Mapillary’s data, let’s have a small explanation of how the API works. It provides 3 ways to access its data: 
1. _[Images API](https://www.mapillary.com/developer/api-documentation/#images):_ it returns the images from a spatial parameter (within a delimited square or a point with a radius).
2. _[Object detections API](https://help.mapillary.com/hc/en-us/articles/115000967191-Object-detections):_ it is a way to query by the content of the images.
3. _[Map Features API](https://www.mapillary.com/developer/api-documentation/#map-features):_ returns locations of objects as point features on the map extracted from multiple images.

![Segmentation of Maxvorstadt in Mapillary](/images/blog/high_data_quality/mapillary_fig2.webp "Maxvorstadt")_Figure 2 Segmentation of Maxvorstadt and Mapillary's algorithm_

One of our first uses of Mapillary’s API was to create a map of Maxvorstadt, Munich, by using different segments from the Object Detections API. In this case, we looked for images showing cars, the sky, vegetation, and sidewalks. Since Mapillary’s algorithm breaks the image into 65 classes of objects as shown in Figure 2, we extracted the images with the highest proportion of the classes of interest. 

As a result, as shown on the map Figure 2, it is also possible to identify streets with high vegetation, or dense parking offer. It is interesting to see how multiple streets have a high percentage of “sky”. This may be due to wide streets and large open spaces, such as around the Pinakothek, or simply because most cameras were pointing to the sky.

## Automation algorithm

Either way, we went even further! We did not want to analyze only one neighborhood in Munich. We wanted to capture the entire city, or even extend to [other cities where GOAT is currently in use](../../goatlive/). Our first challenge was to call the API for larger areas.

To overcome it, we developed a function to divide the area into a grid of smaller squares. The function also incorporates tiny time breaks in between the squares, so we would not overload the servers. Afterward, we join the extracted information from all the squares into a single JSON file.

The second challenge was related to the parameter for the API. Depending on the data required, the API needs a different set of parameters that has to be changed manually. To solve it, we filtered our own library of objects from the complete list of the [Mapillary API Documentation](https://www.mapillary.com/developer/api-documentation/), this filtered library is within a YAML file, which has all the parameters required for the API.

Now, in a single run, the script can call multiple objects either from the Object detection API or the Map Features API. For a deeper understanding, we invite you to take a look into our work, in our [GitHub repo](https://github.com/goat-community/mapillary-api). Finally, the idea is to set these functions into a Lambda function on Amazon Web Services (AWS) with temporal and event triggers.

## Making use of the data

And how are we going to use this information? For accessibility and walkability analysis. Currently, we have used the data from Mapillary to obtain a better data basis for the [Walkability Index](/posts/2021-04-06-walkability-index/) and in this course we have collected more than 20,000 images in the city of Freiburg.

But there are also many other potential applications. Let's assume we are analyzing perceived walking accessibility in a neighborhood at night. In this type of analysis, we are interested in factors that influence the attractiveness of walking. In this case, that would be lighting. We can retrieve this information, represented by the presence of streetlights, through the Mapillary API, improving the accuracy of the analyses.

Another use case could be the improvement of urban green in a city. With the object detection function it is possible to identify on which streets there is no or little vegetation. These street sections can thus be prioritized in the identification of measures and suitable locations for new trees or facade greening can be found there. 


