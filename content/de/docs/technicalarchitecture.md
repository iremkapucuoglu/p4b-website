---
title: Technische Architektur
permalink: "/de/docs/technicalarchitecture/"
lang: de
sections:
- about
weight: 30

---
#### Systemarchitektur

GOAT ist technisch gesehen eine WebGIS-Anwendung. Die Architektur von GOAT beinhaltet verschiedene Software, einschließlich einer Reihe von Bibliotheken und Programmiersprachen. Das effiziente Zusammenspiel von Software in GOAT wird durch die beliebte klassische Server-Client-Architektur des Web ermöglicht. Wie viele Anwendungen heutzutage verfügt GOAT über eine Datenbank, die eine effiziente Speicherung und Organisation von Informationen ermöglicht. Informationen können somit entsprechend abgerufen, verwaltet und aktualisiert werden. Als Datenbank wird PostgreSQL und die räumliche Erweiterung PostGIS verwendet.

![](/images/docs/about/libraries_used.webp)

Als API wird ein Python Server unter Nutzung des Framworks FastAPI verwendet. So werden Schnittstellen für Geodienste bereitgestellt. Es werden verschiedene Formate unterstützt. Neben dem GeoJSON format werden auch komprimierte Formate wie Geobuf oder Vector tiles verwendet, die eine schnelle Ladezeit im Frontend ermöglichen. Neben den Geodiensten gibt es mehrere Schnittstellen, die für die Business-Logik der Anwendung relevant sind. 

![](/images/docs/about/server_client_architecture.webp)

Das Frontend ist mit dem üblichen Webstack (HTML, CSS, JavaScript) geschrieben. Als Javascript-Framework wird Vue.JS und als räumliche Bibliothek Openlayers verwendet. Die gesamte Software, die in GOAT verwendet wird, ist Open Source und hat eine starke weltweite Akzeptanz und Reputation in der Community. 
