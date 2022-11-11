---
title: Technische Architektur
permalink: "/de/docs/technicalarchitecture/"
lang: de
sections:
- about
weight: 30

---
#### Systemarchitektur

GOAT ist eine WebGIS-Anwendung, die für verschiedene formelle und informelle Planungsprozesse verwendet werden kann. Die Systemarchitektur von GOAT umfasst eine Vielzahl von Software, einschließlich Bibliotheken und Programmiersprachen.

Die effiziente Interaktion der verschiedenen Software in GOAT wird durch die beliebte klassische Server-Client-Architektur des Webs ermöglicht. Wie viele andere Anwendungen heutzutage verfügt GOAT über eine Datenbank, die eine effiziente Speicherung und Organisation von Informationen ermöglicht. 

Auf diese Weise können Informationen in geeigneter Weise abgerufen, verwaltet und aktualisiert werden. Die PostgreSQL-Datenbank wird in Verbindung mit der räumlichen Erweiterung PostGIS verwendet.

![Genutzte Libraries](/images/docs/about/libraries.webp)

Als API wird ein Python Server unter Nutzung des Framworks FastAPI verwendet. So werden Schnittstellen für Geodienste bereitgestellt. Es werden verschiedene Formate unterstützt. Neben dem GeoJSON format werden auch komprimierte Formate wie Geobuf oder Vector tiles verwendet, die eine schnelle Ladezeit im Frontend ermöglichen. Neben den Geodiensten gibt es mehrere Schnittstellen, die für die Business-Logik der Anwendung relevant sind. 

![Server-Client-Architektur](/images/docs/about/server_client_arch.webp)

Das Frontend ist mit dem üblichen Webstack (HTML, CSS, JavaScript) geschrieben. Als Javascript-Framework wird Vue.JS und als räumliche Bibliothek Openlayers verwendet. Auf der Serverseite werden PostgreSQL und PostGIS zur Verwaltung von Geodaten verwendet, und die Conveyal-R5-Engine wird zur Durchführung von Fahrtenanalysen für den öffentlichen Verkehr eingesetzt.
Die gesamte Software, die in GOAT verwendet wird, ist Open Source und hat eine starke weltweite Akzeptanz und Reputation in der Community. 
