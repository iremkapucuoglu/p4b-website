---
title: Isochronen
permalink: "/de/tutorials/isochrone/"
weight: 10
sections:
- training
description: Schritt-für-Schritt-Anleitung für beispielhafte Planungsfragen unter
  Verwendung  der GOAT Isochronen-Funktion.

---
#### Beschreibung des Features

Isochronen sind Isolinien, die alle Punkte verbinden, die von einem bestimmten Startpunkt aus innerhalb eines bestimmten Zeitintervalls erreicht werden können. Sie sind besonders geeignet, um die Erreichbarkeit an einem spezifischen Ort aufzuzeigen. GOAT ermöglicht die Berechnung von Isochronen und erlaubt die Anpassung der Reisegeschwindigkeit, der Reisezeit und des Routingprofils. Gegenwärtig kann zwischen den Routingprofilen „Zu Fuß“, „Fahrrad Standard“, „Fahrrad Pedelec“, „ÖPNV“ und „Auto“ ausgewählt werden. Außerdem kann die Anzahl der zu berechnenden Isochronen eingestellt werden. HELLO TURKEY!

#### Mögliche Anwendungsfälle (Planungsfragen)

* Wie viele Supermärkte können von einem bestimmten Punkt aus innerhalb von 10 Gehminuten erreicht werden?
* Wie viele Menschen können eine ÖV-Haltestelle innerhalb von 5 Minuten mit dem Fahrrad erreichen?
* Wie gut ist die Erreichbarkeit mit dem ÖV im Vergleich zur Erreichbarkeit mit dem Auto?

#### Schritt-für-Schritt-Anleitung für die beispielhaften Planungsaufgaben

#### 1 Erreichbarkeit von Supermärkten

##### 1.1 Planungsfrage

Wie viele Supermärkte können von einem bestimmten Punkt aus innerhalb von 10 Gehminuten erreicht werden?

##### 1.2 Arbeitsschritte

1. Wählen Sie im Menü „Filter Thematische Daten“ die Einrichtung „Supermarkt“ (zu finden in der Kategorie „Einkaufen“).

<img src="/images/tutorials/Isochrone/amenity_supermarket.webp" alt="amenity supermarket" style="max-height:400px;"/>

1. Zoomen Sie zu dem Bereich, in dem Sie die Isochrone berechnen möchten.
2. Wählen Sie das Routingprofil und die gewünschte Gehgeschwindigkeit aus.

<img src="/images/tutorials/Isochrone/Isochrone_1.2_select_de.webp"  alt="choose isochrone range" style="max-height:180px;"/>

1. Platzieren Sie den Startpunkt für die Isochronenberechnung an einem beliebigen Punkt.

<img src="/images/tutorials/Isochrone/starting_point_isochrone.webp"  alt="set starting point" style="max-height:150px;"/>

1. Nachdem die Berechnung ausgeführt wurde, öffnet sich automatisch ein Fenster mit den Ergebnissen. Diesem können Sie die erreichbaren Supermärkte entnehmen.

<img src="/images/tutorials/Isochrone/results_supermarkets.webp"  alt="results"/>

1. Die Ergebnisse können über verschiedene Graphiken analysiert werden. Somit können Sie u.a. die räumliche Verteilung der Supermärkte sehen.

<img src="/images/tutorials/Isochrone/results_supermarkets_2.webp"  alt="results"/>

#### 2 Fahrradrouting

##### 2.1 Planungsfrage

Wie viele Menschen können den Bahnhof innerhalb von 5 Minuten mit dem Fahrrad erreichen?

##### 2.2 Arbeitsschritte

1. Ändern Sie den Routingmodi auf „Fahrrad“ und stellen Sie die Isochronen Reichweite auf 5 Minuten.

<img src="/images/tutorials/Isochrone/Isochrone_2.2_select_de.webp"  alt="Routing mode cycling" style="max-height:180px;"/>

1. Platzieren Sie den Startpunkt für die Isochronenberechnung auf dem Bahnhof.

<img src="/images/tutorials/Isochrone/starting_point_isochrone.webp"  alt="set starting point" style="max-height:150px;"/>

1. Nachdem die Berechnung ausgeführt wurde, erscheint ein Fenster mit den Ergebnissen. Diesem können Sie entnehmen, wie viele Menschen den Bahnhof innerhalb von 10 Minuten mit dem Fahrrad erreichen können.

<img src="/images/tutorials/Isochrone/Isochrone_2.3_10minutes_de.webp"  alt="result"/>

1. Durch das Bewegen des Sliders kann die Reisezeit dynamisch auf 5 Minuten geändert werden.

<img src="/images/tutorials/Isochrone/Isochrone_2.3_5minutes_de.webp"  alt="result"/>

1. Ergänzeng zur Tabelle können die Bevölkerungszahlen in einer Summenkurve visualisiert werden.

<img src="/images/tutorials/Isochrone/Isochrone_2.result_different_graph_Eng.webp"  alt="download" style="max-height:300px;"/>

1. Durch Klicken auf den Download-Button können Sie die Isochronen als GeoJSON, Shapefile oder XML sowie die Ergebnis-Tabelle als Excel-File herunterladen.

<img src="/images/tutorials/Isochrone/Isochrone_2.4_export_de.webp"  alt="download" style="max-height:250px;"/>