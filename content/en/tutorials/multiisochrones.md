---
title: Multiisochrones
permalink: "/tutorials/multiisochrones/"
weight: 20
sections:
- training
description: Step-by-step guide for how to use the multi-isochrones feature in GOAT
  for an exemplary planning task.

---
#### Description of the feature

GOAT enables the calculation of multi-isochrones, which show how many residents from a certain neighbourhood have access to a facility (e.g. supermarket, kindergarten, public transport stop) in a certain travel time.

#### Possible use cases (planning questions)

* How well are the supermarkets currently distributed over the city? In which districts do you have accessibility deficits?
* How many inhabitants can reach a public transport stop by bicycle in a given travel time?

#### Step-by-step tutorial for an exemplary planning task

##### 1 Accessibility to supermarkets

###### 1.1 Planning question

How well are the supermarkets currently distributed over the city? In which districts do you have accessibility deficits?

###### 1.2 Step-by-Step guide

1. Display the supermarkets as thematic data.

<img src="/images/training_materials/Multiisochrones/amenity_supermarket.webp"  alt="Thematic Data" style="max-height:250px;"/>

2. Switch to the "Multiple" isochrone calculation mode and select the "Study Area" method, which later lists all results differentiated by districts.

<img src="/images/training_materials/Multiisochrones/multi.webp"  alt="Multi Isochrone" style="max-height:350px;"/>

3. Then select all districts that you want to include in the calculation by clicking on the map.

![Select Districts](/images/training_materials/Multiisochrones/select_study_area.webp)

4. Click on "Calculate."

<img src="/images/training_materials/Multiisochrones/calculate.webp"  alt="Calculate" style="max-height:345px;"/>

5. The resulting multi-isochrones shows the catchment areas of the supermarkets (here for the mode "pedestrian" with 5 minutes catchment area in light green and 10 minutes catchment area in dark green). The corresponding table shows, sorted by district, how many people out of the total population can reach a supermarket in 5 or 10 minutes walking distance.

![Result](/images/training_materials/Multiisochrones/result_multiisochrone.webp)