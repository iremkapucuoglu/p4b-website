---
title:  Scenarios - Buildings
permalink: /tutorials/scenario-buildings/
weight: 50
sections:
  - training
---

#### Description of the feature
GOAT allows the development of own scenarios for changes in the building structure, such as the construction of a new residential area or the demolition of an old building. The developed scenario can be added to the existing urban structure and the changes in accessibility can be evaluated. 

#### Possible use cases (planning questions)
- How does a new residential area effect the accessibility to schools in a certain neighbourhood?
- Is the population in a new residential area served with the everyday necessities?
- Where is the potential for further settlement development?

#### Step-by-step tutorial for the exemplary planning task
##### 1 Scenario on new residential development
###### 1.1 Planning question
- How many additional residents have access to a primary school within a 10-minute walk if an existing residential area will be redensified?


###### 1.2 Step-by-Step guide
1. Display the layer "Buildings" from the category "Buildings and landuse" and the layer "Population" from the category "Accessibility". These show all existing buildings (in red: buildings with residential use, in white: buildings without residential use) and the population density (the darker the background, the higher the population density).  

![Buildings layer](/images/training_materials/Scenario_buildings/building_layer.webp)

2. Navigate to the scenario development menu and create a new scenario.  

<img src="/images/training_materials/Scenario_POIs/create_scenario.webp" alt="New scenario" style="max-height:150px;"/>

3. Give the scenario a name and click on "OK".  

<img src="/images/training_materials/Scenario_buildings/name_scenario.webp" alt="Name scenario" style="max-height:200px;"/>

4. Select which layer you want to edit, in this case the "Buildings" Layer.  

<img src="/images/training_materials/Scenario_buildings/scenario_buildings.webp" alt="Edit Buildings" style="max-height:250px;"/>

5. Using the editing tools, you can draw and edit new buildings. Specify the type of use and the number of floors for each new building. In addition, you must set at least one entrance for each building. Once you have done this, the building will appear in green.  

![Draw Buildings](/images/training_materials/Scenario_buildings/draw.webp)

6. In order to integrate the modified buildings into the database, they must be uploaded using the "Upload" button.  

<img src="/images/training_materials/Scenario_buildings/upload.webp" alt="Upload Buildings" style="max-height:250px;"/>

7. Change to the scenario view. By scrolling the map, the heatmap for population density is updated. The changed population is now included in the calculation.  

![Scenario View](/images/training_materials/Scenario_buildings/scenario_heatmap.webp)

8. Display the primary schools as Thematic Data.   

9. Switch to the Isochrone Menu, change to the comparison mode, select the "Multiple" isochrone calculation mode and the "Study Area" method.  

<img src="/images/training_materials/Scenario_buildings/multiisochrones.webp" alt="Comparison multi isochrone" style="max-height:250px;"/>

10. Select the district on the map where you have carried out the redensification with a mouse click.

11. Click on "Calculate".  

<img src="/images/training_materials/Scenario_buildings/calculate.webp" alt="Calculation" style="max-height:250px;"/>

12. The resulting multi-isochrones show the catchment areas of the primary schools (here for the mode "pedestrian" with 5-minutes catchment area in light green and 10-minutes catchment area in dark green). The associated table shows how many additional people now live in the 5- and 10-minute catchment area of a primary school as a result of the redensification.  

![Result](/images/training_materials/Scenario_buildings/result.webp)

 