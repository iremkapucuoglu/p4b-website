---
title:  Szenarien - Standortplanung
permalink: /de/tutorials/scenario-location/
weight: 40
sections:
- training
---

#### Beschreibung des Features
GOAT ermöglicht die Entwicklung eigener Szenarien zur Standortplanung, so kann ein bspw. ein neuer Supermarkt oder eine neue Schule hinzugefügt werden und die Auswirkungen auf die Erreichbarkeit mithilfe von Heatmaps und Multi-Isochronen ermittelt werden. 

#### Mögliche Anwendungsfälle (Planungsfragen)
- Wie verändert sich die Erreichbarkeit zu Supermärkten in einer Nachbarschaft, wenn den Standort eines Supermarktes verändert wird?
- Wie verändert sich die Erreichbarkeit zu Schulen, wenn eine neue Schule hinzugefügt wird?
- Wie gut sind die Kindergärten über die Stadt verteilt? Wo wäre eine gute Position für einen neuen Kindergarten? 


#### Schritt-für-Schritt-Anleitung für eine beispielhafte Planungsaufgabe
##### 1 Szenario zum Bau eines neuen Kindergartens
###### 1.1 Planungsfrage
- Wie gut sind die Kindergärten aktuell über die Stadt verteilt? 
- In welchen Stadtteilen gibt es Defizite in der fußläufigen Erreichbarkeit? 
- Und wie könnten diese behoben werden?
- Wo wäre eine gute Position für einen neuen Kindergarten? 


###### 1.2 Arbeitsschritte
1. Lassen Sie sich als Thematische Daten die Kindergärten anzeigen.  

<img src="/images/training_materials/Scenario_POIs/kindergarten.webp" alt="Amenity kindergarten" style="max-height:200px;"/>

2. Blenden Sie die Heatmap „Vergleich von Erreichbarkeit und Bevölkerungsdichte” ein. Dieser zeigt, wie gut die fußläufige Erreichbarkeit zu den gewählten Zielen räumlich über die Bevölkerung verteilt ist. Die rote Färbung zeigt Räume auf mit einem Unterangebot.  

![Comparison heatmap](/images/training_materials/Scenario_POIs/walkability_popoulation_index.webp)

3. Gehen Sie nun in das Fenster zur Szenarienentwicklung und erstellen ein neues Szenario.  

<img src="/images/training_materials/Scenario_POIs/create_scenario.webp"  alt="New scenario" style="max-height:150px;"/>

4. Geben Sie dem Szenario einen Namen und klicken Sie auf "OK".  

<img src="/images/training_materials/Scenario_POIs/name_scenario.webp" alt="Name scenario" style="max-height:200px;"/>

5. Wählen Sie den zu bearbeitenden Layer aus, in diesem Fall den „Point of Interest” Layer.  

<img src="/images/training_materials/Scenario_POIs/PointofInterest.webp" alt="Edit POIs" style="max-height:200px;"/>

6. Bearbeiten Sie die Kindergärten so (bestehende Kindergärten verschieben oder neue Kindergärten hinzufügen), dass auch die Stadtteile mit Erreichbarkeitsdefiziten abgedeckt werden. Um einen Kindergarten zu verschieben, müssen sie diesen zunächst über das Kreis-Werkzeug auswählen.

<img src="/images/training_materials/Scenario_POIs/circle_tool.webp" alt="Edit Kindergartens" style="max-height:270px;"/>

7. Schalten Sie zur "Szenario" Ansicht.  

<img src="/images/training_materials/Scenario_POIs/scenario_heatmap.webp" alt="Scenario View" style="max-height:250px;"/>

8. Durch Scrollen der Karte aktualisiert sich die Heatmap „Vergleich von Erreichbarkeit und Bevölkerungsdichte”. Die veränderten Kindergärten werden nun in die Berechnung mit einbezogen.  

![Scenario Heatmap](/images/training_materials/Scenario_POIs/new_kindergarden.webp)

