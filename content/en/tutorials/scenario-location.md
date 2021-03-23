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
![](/images/training_materials/Scenario_POIs/kindergarten.png)

2. Display the layer "Walkability-Population-Index" from the "Accessibility" layers. This shows how well the walking accessibility to the selected destinations is spatially distributed over the population. Blue coloring means oversupply and red coloring means undersupply. Areas shown in yellow indicate that existing supply and population are balanced.  
![](/images/training_materials/Scenario_POIs/walkability_popoulation_index.png)

3. Now go to the menu for scenario development and create a new scenario.  
![](/images/training_materials/Scenario_POIs/create_scenario.png)

4. Give the scenario a name and click on "OK".  
![](/images/training_materials/Scenario_POIs/name_scenario.png)

5. Select which layer you want to edit, in this case the "Point of Interest" Layer.  
![](/images/training_materials/Scenario_POIs/PointofInterest.png)

6. Edit the kindergartens (move existing kindergartens or add new kindergartens) in such a way that the districts with accessibility deficits are also covered. To move a kindergarten, you must first select it using the circle tool.  
![](/images/training_materials/Scenario_POIs/circle_tool.png)

7. Change to the scenario view.  
![](/images/training_materials/Scenario_POIs/scenario_heatmap.png)

8. By scrolling the map, the heatmap for the walkability population index is updated. The changed kindergartens are now included in the calculation. 
![](/images/training_materials/Scenario_POIs/new_kindergarden.png)








 