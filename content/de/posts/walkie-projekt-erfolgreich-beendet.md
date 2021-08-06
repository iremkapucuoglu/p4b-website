+++
author = ""
categories = []
date = ""
description = ""
draft = true
image = ""
summary = ""
thumbnail = ""
title = "WALKIE Projekt erfolgreich beendet "
translationKey = ""

+++
## Neue Features von GOAT: Walkability Index und Fußgängerpotenzialströme

Zu Fuß gehen ist die wohl nachhaltigste Form der Mobilität, denn es ist ökologisch, sozial, ökonomisch und basiert somit auf allen drei Säulen der Nachhaltigkeit. Dafür ist eine sichere und komfortable Fußgängerinfrastruktur notwendig - und zur Verbesserung dieser haben wir einen Walkability Index entwickelt. 

Im Rahmen des Projektes [WALKIE](https://plan4better.de/posts/2021-04-06-walkability-index/) („WALKability IndEx“) haben wir eine dreimonatige Förderung durch das [Verkehrsministerium Baden-Württemberg](https://vm.baden-wuerttemberg.de/de/startseite/) im Rahmen der Anschlussförderung des [MobiDataBW Hackathons 2020](https://vm.baden-wuerttemberg.de/de/politik-zukunft/zukunftskonzepte/digitale-mobilitaet/mobidata-bw-hackathon/) erhalten. Diese ermöglichte uns den Index in enger Zusammenarbeit mit der Pilotkommune [Freiburg](https://digital.freiburg.de/) zu konkretisieren und im Anschluss erfolgreich auf diese zu übertragen. 

Somit haben wir sowohl alle angegebenen Meilensteine als auch das Hauptziel erreicht! GOAT wurde auf eine neue Stadt übertragen und konnte um neue Features erweitert werden, welche sowohl die aktuelle Fußgängerfreundlichkeit (engl. Walkability) der Städte, als auch Verbesserungspotenziale, priorisiert darstellen können.

## Konkretisierung des Walkability-Index:

Das digitale Webtool GOAT war zuvor bereits in der Lage, die Verfügbarkeit von Gehwegen darzustellen. Mit der Einbindung des Walkability Indexes wird nun auch die Attraktivität für Fußgänger berücksichtigt. 

Die Idee zur Entwicklung von WALKIE sowie ein erster Prototyp entstanden im Rahmen des MobiDataBW Hackathons im November 2020. Das Team nutzte die darauffolgende Innovationsphase (März-Juni 2021) zur Weiterentwicklung und Verstetigung der Funktionen, mit der Stadt Freiburg als Pilotstandort. WALKIE ist nun ein aussagekräftiger, multi-kriterieller Walkability Index, der die Attraktivität des Zufußgehens quantitativ abbildet.

Zunächst wurden auf Basis bestehender wissenschaftlicher Erkenntnisse die Qualitätskriterien der Walkability sowie deren Gewichtungen ermittelt. Als Resultat wurde der Walkability Index mit sechs Kategorien, die in 22 Sub-Indikatoren unterteilt sind, entwickelt.

Die Walkability-Kategorien:

* Gehkomfort
* Schutz vor dem Straßenverkehr
* Beleuchtung & subjektive Sicherheit
* Belebtheit & Gehumgebung
* Vegetation & Gewässer
* Urbane Ausstattung

Die zahlreichen Einzelindikatoren wurden in einem Algorithmus bewertet, gewichtet und zu einem Gesamt-Walkability-Score aggregiert. Dabei wurden Scores zwischen 0 und 100 errechnet, wobei 0 eine niedrige und 100 eine hohe Fußgängerfreundlichkeit bedeuten.

Wir haben unterschiedliche Datenquellen benutzt. Zum einen durch Crowdsorcing erhobene Datensätze, aber auch die OpenData-Plattformen von Stadt und Land (z.B. [FreiGIS](https://geoportal.freiburg.de/freigis/)). Darüber hinaus haben wir für die Stadt Freiburg über 10.000 Bildaufnahmen des Straßenraums über die Plattform [Mapillary](https://www.mapillary.com/) erhoben. 

Daraus konnten wir u.a. Infos zu den verschiedenen Attributen der Straßen oder zum Vorhandensein von Straßenlaternen, Parkbänken, etc. herauslesen. Besonders innovativ war dabei die Nutzung der Mapillary-API: automatisierte KI-Algorithmen erkennen und lesen die Objekte aus den Bildsequenzen aus. In [diesem Blogartikel](https://plan4better.de/de/posts/2021-15-06-high-quality-data-now-automatic/ "Automatisierte Bilderkennung") erklären wir genauer, wie wir Mapillary für die automatisierte Objekterkennung für die einzelnen Wegabschnitte in Freiburg genutzt haben.

_Bild_

Die enge und konstruktive Zusammenarbeit mit der Pilotstadt Freiburg war erheblich für die Entwicklung von WALKIE und den erfolgreichen Projektverlauf. Dazu hat sich das Team mehrmals mit Vertretenden der Einheit DIGIT (Digitales und IT) der Stadt Freiburg getroffen und ihr Feedback in den Entwicklungsprozess von WALKIE eingebunden. Außerdem wurden die lokal verfügbaren Daten in GOAT eingebunden und eine [auf die Stadt Freiburg abgestimmte GOAT-Version](https://freiburg.open-accessibility.org/) entwickelt.

In dieser GOAT-Version wurde auch der Walkability Index erstmals veröffentlicht. Somit kann pro Wegabschnitt in Freiburg die Walkability dargestellt werden. Die grünen Wege haben einen hohen Score, d.h. sie sind besonders fußgängerfreundlich. Bei orangenen Wegen ist ein niedriger Walkability Score berechnet und es besteht somit Verbesserungspotenzial. So können Schwachstellen sehr gut und verständlich visualisiert werden.

_Bild_

## Fußgängerpotenzialströme – Welche Straßen sind hoch frequentiert?