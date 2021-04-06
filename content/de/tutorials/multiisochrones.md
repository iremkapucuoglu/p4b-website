---
title:  Multiisochronen
permalink: /de/tutorials/multiisochrones/
weight: 20
sections:
  - training
---

#### Beschreibung des Features
GOAT ermöglicht die Berechnung von Multi-Isochronen. In Verbindung mit Bevölkerungsdaten kann so binnen Sekunden der Anteil der Bevölkeruung identifiziert werden, der in eine gewissen Reisezeit Zugang zu Einrichtung wie Supermärkten, Kindergärten, ÖV-Haltestellen etc. hat.


#### Mögliche Anwendungsfälle (Planungsfragen)
- Wie gut sind die Supermärkte aktuell über die Stadt verteilt? In welchen Stadtteilen gibt es Erreichbarkeitsdefizite?
- Wie viele Bewohner können in einer bestimmten Reisezeit mit dem Fahrrad ÖV Haltestelle erreichen?


#### Schritt-für-Schritt-Anleitung für eine beispielhafte Planungsaufgabe
##### 1 Erreichbarkeit von Supermärkten
###### 1.1 Planungsfrage
Wie gut sind die Supermärkte aktuell über die Stadt verteilt? In welchen Stadtteilen gibt es Erreichbarkeitsdefizite?


###### 1.2 Arbeitsschritte
1. Lassen Sie sich als Thematische Daten die Supermärkte anzeigen.  

<img src="/images/training_materials/Multiisochrones/amenity_supermarket.webp"  alt="Thematic Data" style="max-height:250px;"/>

2. Wechseln Sie zum Isochronenberechnugsmodus „Multi“ und wählen die Methode „Ortsteil“ aus, diese wird später alle Ergebnisse nach Ortsteilen differenziert auflisten.  

<img src="/images/training_materials/Multiisochrones/multi.webp"  alt="Multi Isochrone" style="max-height:350px;"/>

3. Wählen Sie dann per Mausklick alle Ortsteile in der Karte.

![Select Districts](/images/training_materials/Multiisochrones/select_study_area.webp)

4. Klicken Sie auf „Berechnen“.  

<img src="/images/training_materials/Multiisochrones/calculate.webp"  alt="Calculate" style="max-height:345px;"/>

5. Die resultierenden Multi-Isochronen zeigen Ihnen die Einzugsbereiche der Supermärkte (hier für den Modus „Fußgänger“ mit 5 Minuten Einzugsbereich in hellgrün und 10 Minuten Einzugsbereich in dunkelgrün). Die zugehörige Tabelle zeigt nach Ortsteil sortiert, wie viele Menschen von der Gesamtbevölkerung in 5 bzw. 10 Minuten Zufußgehen einen Supermarket erreichen können.  

![Result](/images/training_materials/Multiisochrones/result_multiisochrone.webp)











 