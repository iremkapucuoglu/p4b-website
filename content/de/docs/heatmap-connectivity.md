---
title: Heatmap - Konnektivität
permalink: "/de/docs/heatmap-connectivity/"
lang: de
sections:
- technical
weight: 60
---

In GOAT gibt es eine Heatmap, die die Konnektivität des Gebiets zeigt, d.h. wie gut das Wegenetz miteinander verbunden ist. Dies ist besonders wichtig für die Förderung aktiver Verkehrsträger (Fußgehen und Radfahren), da diese Verkehrsträger Umweg-empfindlich sind. Für die Visualisierung wird ein hexagonales Gitter verwendet.

![GOAT Heatmap Konnektivität](/images/docs/technical_documentation/connectivity/connectivity.webp "GOAT Heatmap Konnektivität")

#### Berechungsmethode

Ausgehend vom Mittelpunkt eines jeden Hexagons werden drei Isochronen berechnet (5 min, 10 min und 15 min). Die durchschnittliche Fläche aller drei Isochronen wird mit den Werten der anderen Hexagonen verglichen. Anhand von Quintilen werden die Ergebnisse klassifiziert.

![Berechnungsmethode](/images//docs/technical_documentation/connectivity/isochrone_en.webp "Berechnungsmethode")
