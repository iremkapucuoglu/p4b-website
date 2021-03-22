---
title: Szenarien - Wege
permalink: /de/tutorials/scenario-ways/
weight: 30
sections:
- training
---

#### Beschreibung des Features
GOAT ermöglicht die Entwicklung eigener Szenarien, wie z.B. Modifikation des Netzwerks oder Bau einer neuen Brücke. Das entwickelte Szenario kann zu dem aktuellen Netzwerk hinzugefügt und Änderungen der Erreichbarkeit durch Isochronen bewertet werden. 

#### Mögliche Anwendungsfälle (Planungsfragen)
- Wie verändert sich die Erreichbarkeit durch den Bau einer neuen Fahrradbrücke über einen Fluss?
- Wie verändert sich die Erreichbarkeit mit dem Rollstuhl durch den Bau einer barrierefreien Wegeverbindung? 
- Welche Variante eines neuen Radweges erschließt die höchste Anzahl an Anwohner?


#### Schritt-für-Schritt-Anleitung für eine beispielhafte Planungsaufgabe
##### 1 Szenario zu neuer Fahrradbrücke
###### 1.1 Planungsfrage
Wie verändert sich die Erreichbarkeit durch den Bau einer neuen Fahrradbrücke über einen Fluss? 
###### 1.2 Arbeitsschritte
1. Gehen Sie in das Fenster zur Szenarienentwicklung und erstellen Sie ein neues Szenario.  
![](/images/training_materials/Scenario_POIs/create_scenario.png)

2. Geben Sie dem Scenario einen Namen und klicken Sie auf "OK".  
![](/images/training_materials/Scenario_POIs/name_scenario.png)

3. Wählen Sie welchen Layer Sie bearbeiten möchten, in diesem Fall den „Wege“ Layer.  
![](/images/training_materials/Scenario_building/name_scenario.png)


4. Zoomen Sie zu der Stelle, an der Sie eine neue Fahrradbrücke bauen wollen und wählen Sie mittels des Kreis-Werkzeuges das umliegenden Straßennetz aus.
![](/images/training_materials/Scenario_building/circle_scenario.png)

5. Zeichnen Sie an der gewünschten Stelle eine neue Wegeverbindung, wählen als Wegetyp „Brücke“ aus und klicken Sie auf „Speichern“. Die gezeichneten Wege werden nun rechts in der Tabelle aufgeführt. Um diese Wege in die Datenbank zu integrieren, müssen diese über den Button „Hochladen“ hochgeladen werden.  
![](/images/training_materials/Scenario_building/bridge_building.png)


6. Nun können Sie die Auswirkung der neuen Wegeverbindung auf die Erreichbarkeit analysieren, indem Sie sich die Standard- und die Scenario-Isochrone berechnen lassen. Wählen Sie hierzu den Routingmodi „Fahrrad“ aus und setzen den Berechnungsmodus auf „Vergleich“. In den Optionen können Sie die Reisezeit, die Fahrgeschwindigkeit und die Anzahl der zuberechnenden Isochronen einstellen.  
![](/images/training_materials/Scenario_building/comparison.png)

7. Platzieren Sie den Startpunkt für die Isochronenberechnung in der Nähe der neuen Brücke. Als Ergebnis wird Ihnen in Rot die Isochrone in der Ausgangslage und in Grün die Isochrone unter Berücksichtigung der neuen Wegeverbindung angezeigt.  
![](/images/training_materials/Scenario_building/result-isochrone.png)

