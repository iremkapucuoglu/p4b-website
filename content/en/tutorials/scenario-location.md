---
title: Scenarios - Location Planning
permalink: "/tutorials/scenario-location/"
weight: 40
sections:
- training

---
#### Description of the feature

GOAT allows you to develop your own location planning scenarios, for example, add a new supermarket or school and determine the impact on accessibility using heat maps and multi-isochrones.

#### Possible use cases (planning questions)

* How does accessibility to supermarkets in a neighbourhood change when the location of a supermarket is changed?
* How does accessibility to schools change when a new school is added?
* How well are the kindergartens distributed throughout the city? Where would be a good location for a new kindergarten?

#### Step-by-step tutorial for the exemplary planning task

##### 1 Scenario on accessibility to kindergartens

###### 1.1 Planning questions

* How well are kindergartens currently distributed across the city?
* In which parts of the city are there deficits in pedestrian accessibility?
* And how could these be remedied?
* Where would be a good location for a new kindergarten?

###### 1.2 Step-by-Step guide

1. Select the kindergartens as Thematic Data.

<img src="/images/training_materials/Scenario_POIs/kindergarten.webp" alt="amenity kindergarten" style="max-height:200px;"/>

1. Display the heatmap "Accessibility and Population Density." This shows how well the walking accessibility to the selected destinations is spatially distributed over the population. The red coloring indicates spaces that are currently undersupplied.
2. Now go to the menu for scenario development and create a new scenario.

<img src="/images/training_materials/Scenario_POIs/create_scenario.webp"  alt="new scenario" style="max-height:150px;"/>

1. Give the scenario a name and click "OK".

<img src="/images/training_materials/Scenario_POIs/name_scenario.webp" alt="name scenario" style="max-height:200px;"/>

1. Select the layer you want to edit, in this case the "Point of Interest" Layer.

<img src="/images/training_materials/Scenario_POIs/PointofInterest.webp" alt="edit POIs" style="max-height:200px;"/>

1. Edit the kindergartens (move existing kindergartens or add new kindergartens) to cover the neighborhoods with accessibility deficits. To move a kindergarten, you must first select it using the circle tool.

<img src="/images/training_materials/Scenario_POIs/circle_tool.webp" alt="edit Kindergartens" style="max-height:270px;"/>

1. Switch to the "Scenario" view.

<img src="/images/training_materials/Scenario_POIs/scenario_heatmap.webp" alt="edit Kindergartens" style="max-height:250px;"/>

1. Scrolling the map updates the "Comparison of Accessibility and Population Density" heatmap. The modified kindergartens are now included in the calculation.