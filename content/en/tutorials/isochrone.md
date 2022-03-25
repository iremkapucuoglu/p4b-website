---
title: Isochrones
permalink: "/tutorials/isochrone/"
weight: 10
sections:
- training
description: Possible use cases and step-by-step tutorials for exemplary planning
  cases for the GOAT isochrone feature.

---
#### Description of the feature

Isochrones are isolines connecting all points that can be reached from a specific starting point within a certain time interval. GOAT allows the calculation of isochrones that take factors such as speed, infrastructure network, and traveling time into account. This can be adjusted automatically by choosing between the following modes: walking (standard or elderly), cycling, and wheelchair. Isochrones can be used as an indicator of accessibility in one specific location.

#### Possible use cases (planning questions)

* How many supermarkets can be reached from a certain point in a 10-minute walk?
* How many people can access a public transport station within 5 minutes of cycling?

#### Step-by-step tutorials for exemplary planning tasks

#### 1 Accessibility to supermarkets

##### 1.1 Planning question

How many supermarkets can be reached from a certain point in 10 minutes walking?

##### 1.2 Step-by-Step guide

1. Display all supermarkets by enabling the amenity "Supermarket" in the Thematic Data Filter under the category "Shop".

![](/images/isochroneeng1.png)

1. Zoom in into the area where you want to calculate the isochrone.
2. Set the isochrone range to 10 minutes.

![](/images/isochroneeng2.png)

1. Place the starting point for the isochrone.
2. After the calculation has been carried out, a window with the results opens automatically. From this window you can see the number of supermarkets that can be reached within 10 minutes.

![](/images/isochroneeng3.png)

#### 2 Bicycle Routing

##### 2.1 Planning question

How many people can reach the train station within 5 minutes by bike?

##### 2.2 Work steps

1. Change the routing mode to “cycling”.

![](/images/training_materials/Isochrone/cycling_mode.png)

1. Set the isochrone range to 5 minutes.
2. Place the starting point for the isochrone calculation on the station.

<!-- ![](/images/training_materials/Isochrone/starting-point-isochrone.webp) -->
<img src="/images/training_materials/Isochrone/starting-point-isochrone.webp"  alt="set starting point" style="max-height:150px;"/>

1. After the calculation has been carried out, a window with the results opens automatically. From this window you can see the population that can reach the train station within 5 minutes of cycling.

![Reached population](/images/training_materials/Isochrone/isochrone_trainstation.webp)