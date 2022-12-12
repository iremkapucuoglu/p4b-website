---
title: Heatmap - Konnektivität
permalink: "/de/docs/heatmap-connectivity/"
lang: de
sections:
- technical
weight: 60
---

Verschiedene Indikatoren dienen als Benchmark für die Wegekonnektivität und die lokale Erreichbarkeit bei der Planung von fußgänger- und fahrradfreundlichen Quartieren. Einer dieser Indikatoren ist die Konnektivitäts-Heatmap. Die Konnektivitäts-Heatmap in GOAT ermöglicht es dem Benutzer, den Grad der Konnektivität des wegenetzes im Untersuchungsgebiet zu analysieren. Dies ist besonders wichtig für die Förderung aktiver Verkehrsträger (Zufußgehen und Fahrradfahren), da diese Verkehrsträger empfindlich auf Umwege reagieren.

![GOAT Heatmap Konnektivität](/images/docs/technical_documentation/connectivity/connectivity_en_2.webp "GOAT Heatmap Konnektivität")

#### Berechungsmethode

Die Heatmap wird unter Verwendung eines hexagonalen Rasters mit einer ungefähren Kantenlänge von 150 m pro Rasterzelle für den Modus "Gehen" (5 km/h) berechnet.

<img src="\images\docs\technical_documentation\connectivity\hexagonal_en.webp" alt="hexagonal" style="max-height:380px;"/>

Ausgehend vom Mittelpunkt eines jeden Hexagons werden drei Isochronen berechnet (5 min, 10 min und 15 min). Die Größe aller drei Isochronen wird in m² wird pro Zelle berechnet:
<i>(durchschnittliche_Isochronenfläche = (isochrone1_fläche + isochrone2_fläche + isochrone3_fläche) / 3)</i>
und mit allen anderen Rasterzellen anhand statistischer Quintile verglichen. 

Die Rasterzellen sind von hoher (grün) bis niedriger Konnektivität (rot) eingefärbt. Änderungen im Straßennetz werden durch die Neuberechnung von Teilen der Heatmap und die Aktualisierung der statistischen Klassifizierung berücksichtigt. 


