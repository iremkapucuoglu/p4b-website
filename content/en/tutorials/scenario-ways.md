---
title: Scenarios - Ways
permalink: "/tutorials/scenario-ways/"
weight: 30
sections:
- training

---
#### Description of the feature

GOAT allows you to develop your own scenarios, such as network modifications or building a new bridge. The developed scenario can be added to the current network, and changes in accessibility can be evaluated using isochrones.

#### Possible use cases (planning questions)

* How does the construction of a new bicycle bridge across the river change accessibility?
* Which variation of a new bike path provides access to the highest number of residents?

#### Step-by-step tutorial for the exemplary planning task

##### 1 Scenario for a new bicycle bridge

###### 1.1 Planning question

How does the construction of a new bicycle bridge across the river change accessibility?

###### 1.2 Step-by-Step guide

1. Go to the menu for scenario development and create a new scenario.

<img src="/images/training_materials/Scenario_POIs/create_scenario.webp"  alt="Create scenario" style="max-height:150px;"/>

1. Give the scenario a name and click "OK".

<img src="/images/training_materials/Scenario_building/name_scenario.webp"  alt="Name scenario" style="max-height:200px;"/>

1. Select the layer you want to edit, in this case the "Ways" Layer.

<img src="/images/training_materials/Scenario_building/scenario_ways.webp"  alt="Edit ways" style="max-height:300px;"/>

1. You're now in the scenario mode. To indicate the new mode, the menu color changes from green to dark blue.
2. Zoom to the location where you want to build a new bicycle bridge and select the surrounding road network using the circle tool.

<img src="/images/training_materials/Scenario_building/circle_scenario.webp"  alt="Circle toot" style="max-height:300px;"/>

1. Draw a new route connection at the desired location, select "Bridge" as the route type and click "Save". The drawn paths are now listed in the table on the right. To integrate these paths into the database, they must be uploaded using the "Upload" button.

<img src="/images/training_materials/Scenario_building/bridge_building.webp"  alt="Draw" style="max-height:300px;"/>

1. Now you can analyze the effect of the new path connection on accessibility by calculating the isochrones for the current state and for the scenario. To do this, select the routing mode "Bike" and set the calculation mode to "Comparison." In the options you can set the travel time, the travel speed and the number of isochrones to be calculated.

<img src="/images/training_materials/Scenario_building/comparison.webp"  alt="Comparison" style="max-height:400px;"/>

1. Place the starting point for the isochrone calculation near the new bridge. As a result you will see in red the isochrones in the actual state and in green the isochrones considering the new path connection. The result table shows the respective area and number of inhabitants within the isochrone.

![](/images/training_materials/Scenario_building/result-isochrone.webp)