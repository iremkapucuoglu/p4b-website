+++
author = ""
categories = ["Daten", "News"]
date = ""
description = ""
draft = true
image = "/images/mapillary_banner.webp"
summary = "Mit der Mapillary API erfolgt der erste Schritt Richtung Automatisierung der Datenerfassung durch die automatische Bilderkennung und Bildsegmentierung. Diese hochwertigen Daten verwendet GOAT bei der Analyse der fußläufigen Erreichbarkeit und Zugänglichkeit."
thumbnail = "/images/mapillary_thumbnail.webp"
title = "Automatisierte Bilderkennung"
translationKey = ""

+++
## Datenherausforderung

Eine der wichtigsten Herausforderungen beim Aufbau eines Planungsinstruments wie GOAT, ist die Verfügbarkeit und Qualität der verwendeten Daten. Wie Sie sich vielleicht erinnern, verwenden wir u.a. [Mapillary](https://www.mapillary.com/) zur Lösung dieses Problems.

Das Mapillary Projekt hat eine erstaunliche Arbeit geleistet, indem sie eine Plattform entwickelt haben, um die Realität in Bildern festzuhalten und vor allem wertvolle Daten aus den Bildern zu extrahieren.

Unsere Geschichte mit Mapillary begann im März 2020, als wir [Fürstenfeldbruck](https://www.open-accessibility.org/mapillary/ "https://www.open-accessibility.org/mapillary/"), eine Stadt 10 km westlich von München, vollständig kartiert haben. Seitdem verwenden wir diese Anwendung zur Verbesserung der Daten, die für unsere Analyse relevant sind. Bis zu diesem Zeitpunkt wurden alle Schritte komplett manuell durchgeführt.

Um immer up-to-date zu bleiben, folgen und lesen wir den Mapillary-Blog. Am 24. August 2020 veröffentlichten sie den Beitrag “[Mapillary map features now available globally in OpenStreetMap](https://blog.mapillary.com/update/2020/08/24/global-map-features-openstreetmap.html)”. Nachdem wir die Updates gelesen haben, legten wir direkt los, um die neuen Funktionen auszuprobieren. Anhand des folgenden Beispiels möchten wir gerne aufzeigen, wie es uns bei unserer Arbeit mit GOAT hilft.

## Mapillary plug-in für JOSM

Im Folgenden teilen wir unsere Erfahrungen mit der Kartierung und Aktualisierung der Fußgängerüberwege in Fürstenfeldbruck. Zuerst haben wir die Basisschicht der  Fußgängerüberwege von [overpass turbo](http://overpass-turbo.eu/) erhalten. In diesem Layer sind die aktuellen Fußgängerüberwege in [OpenStreetMap](https://www.openstreetmap.org/#map=5/50.151/9.539) (OSM) abgebildet. Die Idee war, diese mit den Fußgängerüberwegen zu vergleichen, die vom Mapillary-System identifiziert wurden.

Für diese Analyse haben wir [JOSM](https://josm.openstreetmap.de/) verwendet. Es handelt sich um einen erweiterbaren OSM-Editor für den Desktop, mit dem Funktionen und Attribute der Daten sehr einfach und hoch skalierbar bearbeitet werden können. Innerhalb der JOSM-Schnittstelle ist es jetzt möglich, mithilfe der Mapillary-Funktion, die Ampeln und ihren Standort zu identifizieren.

Darüber hinaus hilft die Street-View-Funktion dabei, die physischen Eigenschaften der Infrastruktur und die Genauigkeit der Position der Verkehrsschilder zu überprüfen. Bei einem Fußgängerüberweg sind uns vor allem die Bestandteile der Infrastruktur wichtig, wie zum Beispiel das Vorhandensein von Zebrastreifen oder einer Verkehrsinsel.

Dementsprechend können die Tags der vorhandenen Infrastruktur aktualisiert werden, damit sie mit den Bildern und Verkehrsschildern übereinstimmen.

![Dieselben Verkehrszeichen an unterschiedlichen Stellen geortet](/images/mapillary_fig1-0.jpg "Zwei Sequenzen mit Verkehrszeichen")_Abbildung 1. Zwei Sequenzen, die dieselben Zeichen an verschiedenen Stellen identifizieren_

Manchmal können jedoch unterschiedliche Sequenzen dieselbe Gruppe von Verkehrsschildern identifizieren, sie jedoch an einer völlig anderen Position lokalisieren (siehe Abbildung 1). Hier zeigt die blaue Sequenz, dass sich die Schilder nach der Rechtskurve (aus Nordosten kommend) befinden, in Wirklichkeit befinden sie sich aber vor der Kurve. In diesem Fall hat die grüne Sequenz sie an einer genaueren Position lokalisiert.

Das Schilder-Identifikationssystem von Mapillary war bereits auf der Website verfügbar, aber das Plug-In in JOSM erleichtert jetzt die Identifizierung und Kartierung erheblich. Es ermöglicht uns in einem größeren Maßstab zu arbeiten und von der JOSM-Benutzeroberfläche  der unterschiedlichen Ebenen zu profitieren, die effektiver ist als der iD-Editor von OpenStreetMap.

Bei diesem Vorgang handelt es sich jedoch noch um eine aufwendige visuelle Überprüfung, bei der viele Schritte übersprungen werden könnten. Mit einem automatisierten Prozess könnte sich die Qualität der Informationen erheblich verbessern.

## Mapillary API: Bildsegmentierung und Objekterkennung

Schon bald nach dem Ausprobieren der Mapillary-Updates, wurde für OSM, am 28. August 2020, eine weitere Funktion veröffentlicht: „Globaler Zugriff auf Kartendaten mit der Mapillary API“. Dies war der erste Schritt zur Automatisierung der Datenerfassung.

Bevor wir Ihnen unsere Arbeit mit den Daten von Mapillary erläutern, möchten wir Ihnen eine kleine Erklärung zur Funktionsweise der API geben: Sie bietet drei Möglichkeiten, auf ihre Daten zuzugreifen: Erstens, „Images API“, es liefert die Bilder von einem räumlichen Parameter (innerhalb eines begrenzten Quadrats oder eines Punkts mit einem Radius). Zweitens, „Object Detections-API“, dies ist eine Möglichkeit, den Inhalt der Bilder abzufragen. Und „Map Features API“, die Positionen von Objekten als Punkt-Features auf der Karte anzeigt, die aus mehreren Bildern extrahiert wurden.![Segmentierung von Maxvorstadt in Mapillary](/images/mapillary_fig2.jpg "Maxvorstadt")_Abbildung 2: Segmentierung von Maxvorstadt und der Algorithmus von Mapillary_

Eine unserer ersten Anwendungen der Mapillary-API war die Erstellung einer Karte von Maxvorstadt, München, unter Verwendung verschiedener Segmente aus der „Object Detections API“. In diesem Fall haben wir nach Bildern, auf denen Autos, der Himmel, Vegetation und Gehwege zu sehen waren, gesucht. Da der Mapillary-Algorithmus das Bild, wie in Abbildung 2 dargestellt, in 65 Objektklassen unterteilt, haben wir die Bilder mit dem höchsten Anteil der relevanten Klassen extrahiert und sie dann mit einer Schätzung der Kernel-Netzwerkdichte mit den Straßen verbunden.

Auf der Karte in Abbildung 2 können daher auch Straßen mit hoher Vegetation oder hohem Parkangebot identifiziert werden. Es ist interessant, dass viele Straßen einen hohen Anteil an „Himmel“ haben. Dies kann an breiten Straßen und großen Freiflächen wie der Pinakothek liegen, oder einfach daran, dass die meisten Kameras in den Himmel gerichtet waren.

## Automatisierungsalgorithmus

Wir wollten nicht lediglich einen Stadtteil in München analysieren, wir wollten die ganze Stadt oder sogar andere Städte, in denen GOAT derzeit arbeitet damit erfassen. Unsere erste Herausforderung bestand darin, die API von größeren Bereichen aufzurufen. Um dies zu überwinden, haben wir eine Funktion entwickelt, mit der der Bereich in ein Raster kleinerer Quadrate unterteilt wird.

Die Funktion beinhaltet auch eine kurze Zeitpause zwischen den Quadraten, damit die Server nicht überlastet werden. Danach verbinden wir die extrahierten Informationen aus allen Quadraten zu einer einzigen .json-Datei.

Die zweite Herausforderung bezog sich auf die Parameter für die API. Je nach benötigten Daten, erfordert die API einen anderen Satz von Parametern, der manuell geändert wird. Um dies zu lösen, haben wir unsere eigene Objektbibliothek aus der vollständigen Liste der Objekte der [Mapillary API-Dokumentation](https://www.mapillary.com/developer/api-documentation/ "https://www.mapillary.com/developer/api-documentation/") herausgefiltert.

Diese gefilterte Bibliothek befindet sich in einer Yaml-Datei und enthält alle für die API erforderlichen Parameter. Jetzt kann das Skript in einem einzigen Durchlauf mehrere Objekte entweder über die Object Detection API oder die Map-Features-API aufrufen.

Für ein tieferes Verständnis laden wir Sie ein, einen Blick auf unsere Arbeit zu werfen, in unserem [Repo](https://github.com/goat-community/mapillary-api "https://github.com/goat-community/mapillary-api") in GitHub. Schließlich besteht das Ziel darin, diese Funktionen in eine Lambda-Funktion in Amazon Web Services (AWS) mit zeitlichen und Ereignisauslösern zu setzen.

## Nutzung der Daten

Und wie werden wir Informationen nutzen? Zur Analyse der Zugänglichkeit und fußläufigen Erreichbarkeit! Nehmen wir an, wir analysieren die fußläufige Erreichbarkeit in einer Nachbarschaft in der Dunkelheit. Bei dieser Art der Analyse interessieren uns Faktoren, die die Entscheidung zum Gehen beeinflussen.

Da der Kontext "zu Fuß gehen in der Dunkelheit” ist, können wir prüfen, ob Menschen einen längeren Umweg machen, um dunklere Straßen zu vermeiden. In diesem Fall wären Laternen die relevanten Objekte der Analyse. Durch diese Informationen könnte die Bewertung genauer sein.

Ein anderes Beispiel könnte eine Stadt sein, die Grünflächen verbessern möchte. Möglicherweise möchten sie ein Projekt zur Verbesserung der Stadtlandschaft durch die Einführung grüner Fassaden durchführen. Mit der Objekterkennungsfunktion ist es möglich, zu identifizieren, auf welchen Straßen keine Vegetation vorhanden ist, und diese im Projekt zu priorisieren.

Diese und viele weitere Anwendungen sind möglich durch die Kombination der hochwertigen Daten von Mapillary mit allen Funktionen, die ein Planungsinstrument wie GOAT bieten kann.

***