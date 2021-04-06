---
title: Testing innovative data collection approaches
author: ramirez
lang: en
tags:
- en
categories:
- development
- data
thumbnail: "/images/blog/sensor_freiberg/plots - thumbnail.webp"
image: "/images/blog/sensor_freiberg/plots - banner.webp"
summary: How does the GOAT-team come to a project for on-street delivery robots? Of
  course, we share the same walking and cycling environment. We used a prototype measuring
  box to automatically detect collect surface and smoothness information of road infrastructure.
date: 2020-11-15

---
## Innovative future

Imagine you are coming out of your house to pick up your food delivery or your Amazon purchase, and surprise! You see Wall-E, the little robot from the Disney movie! What? Well, not exactly. But it may be an autonomous robot delivering one day in the future. Wait, weren’t autonomous vehicles something reserved for cars, trains, or trucks? NO, autonomous vehicles come in different sizes. However, like every self-driving vehicle, they are facing one of the biggest challenges to fully operate: the awareness of the environment where they are moving. For that reason, the team of Prof. Sebastian Zug at the [Chair for Software Technology and Robotics of TU Bergakademie Freiberg](https://tu-freiberg.de/fakult1/inf/professuren/softwaretechnologie-und-robotik) is working on the [project “AK hoch 2“](https://www.bmvi.de/SharedDocs/DE/Artikel/DG/mfund-projekte/akhoch2.html). The project is currently funded by the Federal Ministry of Transport and Digital Infrastructure, to measure the quality and the characteristics of the bicycle infrastructure. Specifically, the goal of the project is to systematically aggregate the parameters of cycleways and footpaths. To achieve it, they created a mobile measuring system that can be set up on any bicycle. It evaluates motion sensors and combines them with position information. Finally, an AI-based classification identifies the type and smoothness of the surface and thereby locates obstacles.

![Measurement box from TU Bergakademie on bicycle](/images/blog/sensor_freiberg/sensors.png "The measurement box developed by the TU Bergakademie Freiberg")

_Figure 1. The measurement box developed by the TU Bergakademie Freiberg_

## Gathering data

How does the GOAT-team come to be part of a project for on-street delivery robots? Of course, we share the same walking and cycling environment. As the main goal of the project is to collect information for cycling and walking infrastructure, we share a very important common interest: reliable and accurate spatial data. For that reason, we have been using the prototype measuring box in our field mapping tasks to collect the information. Here is a sneak peek of going around Munich’s Streets.

![Cycling route in Munich captured with the new measuring device](/images/blog/sensor_freiberg/cyclepath.png "Cycling route captured with the new device")

_Figure 2. Exemplary cycling route that was captured with the measuring device_

The device shows the route ridden, and the user must continuously indicate the category of the infrastructure that they are using (street, bikeway, or pedestrian path).

## Analyzing the measurements

Then the GNSS position is harmonized by a MapMatching algorithm, which compares the derived location with the information available in OpenStreetMap. But the sensor is way more than just GNSS and Speedometer.

![Graphs showing the acceleration in all three dimensions](/images/blog/sensor_freiberg/plots.png "Measured acceleration")

_Figure 3. Measured acceleration in all three dimensions_

The sensor has an accelerometer that measures continuously changes in all three axes plus the vector sum of them. From the acceleration charts, it is possible to identify certain behaviors as acceleration and braking from the changes in the X-axis where below zero would mean braking and over zero is accelerating. Likewise, it is possible to identify a constant vibration in the Y-axis, however, some larger spikes appear in the graph and they may be related to bumps or a rough surface. Finally, and related to the Z-axis, it could be possible to identify sharp changes in the horizontal alignment of the infrastructure or obstacles that may not allow a smooth ride.

Remember [our experience with Mapillary in Fürstenfeldbruck](../2020-04-25-mapillary)? This time we used the same process to have both, the collection of acceleration data, and the street pictures with intervals of 1 second to obtain a better understanding of the road conditions. These first results are very promising and we are looking forward to further use the device in our efforts for better map data.