---
title: Scenarios - Location Planning
permalink: /tutorials/scenario-location/
weight: 40
sections:
  - training
---

#### Description of the feature
GOAT allows you to develop your own Point-of-Interest (POI) scenarios, such as modifying the location of a supermarket or adding a new school. The developed scenario can be added to the current land-use structure, and changes in accessibility can be evaluated by the dynamic heatmap.  

#### Possible use cases (planning questions)
- How does accessibility to supermarkets in a neighbourhood change when the location of a supermarket is changed?
- How does accessibility to schools change when a new school is added?
- How well are the kindergartens distributed throughout the city? Where would be a good position for a new kindergarten? 


#### Step-by-step tutorial for the exemplary planning task
##### 1 Scenario on accessibility to kindergartens
###### 1.1 Planning questions
- How well are the kindergartens currently distributed over the city? 
- In which parts of the city are there deficits in pedestrian accessibility? 
- And how could these be remedied?


###### 1.2 Step-by-Step guide

1. Select the kindergartens as Thematic Data.  

<img src="/images/training_materials/Scenario_POIs/kindergarten.webp" alt="amenity kindergarten" style="max-height:200px;"/>

2. Display the heatmap "Comparison of Accessibility and Population Density". This shows how well the walking accessibility to the selected destinations is spatially distributed over the population. Blue coloring means oversupply and red coloring means undersupply. Areas shown in yellow indicate that existing supply and population are balanced.  

![comparison heatmap](/images/training_materials/Scenario_POIs/walkability_popoulation_index.webp)

3. Now go to the menu for scenario development and create a new scenario.  

<img src="/images/training_materials/Scenario_POIs/create_scenario.webp"  alt="new scenario" style="max-height:150px;"/>

4. Give the scenario a name and click on "OK".  

<img src="/images/training_materials/Scenario_POIs/name_scenario.webp" alt="name scenario" style="max-height:200px;"/>

5. Select which layer you want to edit, in this case the "Point of Interest" Layer.  

<img src="/images/training_materials/Scenario_POIs/PointofInterest.webp" alt="edit POIs" style="max-height:200px;"/>

6. Edit the kindergartens (move existing kindergartens or add new kindergartens) in such a way that the districts with accessibility deficits are also covered. To move a kindergarten, you must first select it using the circle tool.  

<img src="/images/training_materials/Scenario_POIs/circle_tool.webp" alt="edit Kindergartens" style="max-height:270px;"/>

7. Change to the scenario view.  

<img src="/images/training_materials/Scenario_POIs/scenario_heatmap.webp" alt="edit Kindergartens" style="max-height:250px;"/>

8. By scrolling the map, the accessibility population heatmap is updated. The changed kindergartens are now included in the calculation. 

![Scenario Heatmap](/images/training_materials/Scenario_POIs/new_kindergarden.webp)








 