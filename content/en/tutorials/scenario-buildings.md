---
title: Scenarios - Buildings
permalink: "/tutorials/scenario-buildings/"
weight: 50
sections:
- training

---
#### Description of the feature

GOAT allows the development of personalized scenarios for changes in the building structure, such as the construction of a new residential area or the demolition of an old building. The developed scenario can be added to the existing urban structure and the changes in accessibility can be evaluated.

#### Possible use cases (planning questions)

* How does a new residential area effect the accessibility to kindergartens in a certain neighbourhood?
* Is the population in a new residential area served with the everyday necessities?
* Where is the potential for further settlement development?

#### Step-by-step tutorial for the exemplary planning task

##### 1 Scenario on new residential development

###### 1.1 Planning question

* How many additional residents have access to a primary school within a 10-minute walk if an existing residential area will be redensified?

###### 1.2 Step-by-Step guide

1. Display the layer "Buildings" from the category "Buildings and landuse".

<img src="/images/tutorials/Scenario_buildings/Scenarios_buildings_1.2.1_eng.webp" alt="Buildings"/>

2. In addition, enable the heatmap "Population Density". These show all existing buildings (in red: buildings with residential use, in white: buildings without residential use) and the population density (the darker the background, the higher the population density).

<img src="/images/tutorials/Scenario_buildings/Scenarios_buildings_1.2.2_eng.webp" alt="Population"/>

3. Navigate to the scenario development menu and create a new scenario.

<img src="/images/tutorials/Scenario_buildings/Scenarios_buildings_1.2.3_eng.webp" alt="New scenario" style="max-height:280px;"/>

4. Give the scenario a name and click on "OK."

<img src="/images/tutorials/Scenario_buildings/Scenarios_buildings_1.2.4_eng.webp" alt="Name scenario" style="max-height:200px;"/>

5. Select which layer you want to edit, in this case the "Buildings" Layer.

<img src="/images/tutorials/Scenario_buildings/Scenarios_buildings_1.2.5_eng.webp" alt="Edit Buildings" style="max-height:250px;"/>

6. Using the editing tools, you can draw and edit new buildings. Specify the type of use and the number of floors for each new building. In addition, you must set at least one entrance for each building (represented by purple dots). Once you have done this, the building will appear in green.

<img src="/images/tutorials/Scenario_buildings/Scenarios_buildings_1.2.6_eng.webp" alt="Gebäude zeichnen" />

7. Display the kindergartens as Thematic Data.
   
8. Switch to the Isochrone Menu, change to the comparison mode, select the "Multiple" isochrone calculation mode and the "Study Area" method.

<img src="/images/tutorials/Scenario_buildings/Scenarios_buildings_1.2.8_eng.webp" alt="Comparison multi isochrone" style="max-height:400px;"/>

9. Select the district on the map where you have carried out the redensification with a mouse click.
    
10. Click on "Calculate."

<img src="/images/tutorials/Scenario_buildings/Scenarios_buildings_1.2.9and10_eng.webp" alt="Berechnen" style="max-height:310px;"/>

11. The resulting multi-isochrones show the catchment areas of the kindergartens (here for the mode "pedestrian" with 5-minutes catchment area in light green and 10-minutes catchment area in dark green). In this example case, it can be seen in the map that the new population is just at the border of the catchment area and thus has to walk a good 10 minutes to the nearest kindergarten.

<img src="/images/tutorials/Scenario_buildings/Scenarios_buildings_1.2.11_result10min_eng.webp" alt="Ergebnis" />

12. The travel time slider can be adjusted interactively. The multiisochrones are dynamically reacting to the changes. 

<img src="/images/tutorials/Scenario_buildings/Scenarios_buildings_1.2.11_result5min_eng.webp" alt="Ergebnis" />