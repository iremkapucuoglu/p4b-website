---
title: Technische Architektur
permalink: "/de/docs/technicalarchitecture/"
lang: de
sections:
- about
weight: 30

---
#### Systemarchitektur

GOAT ist eine WebGIS-Anwendung, die mit Open-Source-Programmiersprachen und -Bibliotheken erstellt wurde. Sie folgt der traditionellen Server-Client-Architektur, die von Webanwendungen verwendet wird. Dieses vielseitige Werkzeug kann für eine Vielzahl von Planungsfunktionen und -prozessen eingesetzt werden.

![GOAT Server-Client-Architektur](/images/docs/about/server-client-architecture.webp "Server-Client-Architektur")

Die Grundlage der Funktionalität von GOAT ist eine räumliche Datenbank, in der sowohl große räumliche als auch nicht-räumliche Datensätze gespeichert werden können. Eine robuste relationale Datenbank ist für die effiziente Verwaltung, Speicherung und Verarbeitung von Daten unerlässlich. Aus diesem Grund stützt sich GOAT auf PostgreSQL und PostGIS, beides weit verbreitete und ausgereifte Technologien.

GOAT verwendet einen Python-Server als API, unter der Nutzung von FastAPI. Über die API wird die Business-Logik gemanaget, sowie verschiedene Indikatoren in verschiedenen Formaten bereit gestellt. Während die meisten Schnittstellen Daten im JSON-Format bereitstellen, sind auch spezielle Geodatenformate wie Geobuf (z. B. für Heatmaps), eigene Binärformate (z. B. für Isochronen) und Vektor Tiles (z. B. für statische Layer) verfügbar. Insbesondere unterstützt GOAT weitere Geodienste wie WMS und WFS, die den OGC-Standards entsprechen und sich leicht in die Plattform integrieren lassen.

Routing-Funktionalitäten sind für das Backend von GOAT essentiell, da sie zur Berechnung von Reisezeiten für Erreichbarkeitsindikatoren verwendet werden. Für das Gehen und Radfahren implementiert GOAT einen eigens entwickelte Variante des Dijkstra-Algorithmus, während für das Routing von öffentlichen Verkehrsmitteln und Autos die Conveyal R5 Routing Engine verwendet wird. Diese Routing-Engine ist intermodal und kombiniert Straßennetze mit Fahrplandaten, was sie zu einem leistungsstarken Werkzeug für die Erstellung realistischer Reisezeiten macht.

Das Frontend ist in Javascript unter Verwendung des Vue.js-Frameworks erstellt. Für die Bereitstellung von Geodaten wird die Openlayers-Bibliothek verwendet. Das Frontend kommuniziert mit dem Backend, indem es Daten an die API anfordert und sendet. Das Frontend verfügt über umfangreiche Funktionen zur Anzeige und Interaktion mit den Daten. Die gesamte Software, die in GOAT verwendet wird, ist quelloffen und genießt in der weltweiten Community breite Akzeptanz und Ansehen. 

Für das Hosting wird Kubernetes verwendet. Kubernetes ist ein Open-Source-System zur Automatisierung der Bereitstellung, Skalierung und Verwaltung von containerisierten Anwendungen. Es gruppiert die Container, aus denen eine Anwendung besteht, in logische Einheiten, um die Verwaltung und Skalierbarkeit zu erleichtern. Kubernetes ist eine portable, erweiterbare Open-Source-Plattform für die anbieterneutrale Verwaltung von containerisierten Diensten.

