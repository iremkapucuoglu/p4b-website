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

Als API wird ein Python Server unter Nutzung des Framworks FastAPI verwendet. So werden Schnittstellen für Geodienste bereitgestellt. Es werden verschiedene Formate unterstützt. Neben dem GeoJSON format werden auch komprimierte Formate wie Geobuf oder Vector tiles verwendet, die eine schnelle Ladezeit im Frontend ermöglichen. Neben den Geodiensten gibt es mehrere Schnittstellen, die für die Business-Logik der Anwendung relevant sind. 

![GOAT Server-Client-Architektur](/images/docs/about/server-client-architecture.webp "Server-Client-Architektur")

Die üblichen Web-Stack-Anwendungen wie HTML, CSS und JavaScript bilden das Frontend. Um grafische Benutzeroberflächen für Webanwendungen mit HTML-Syntax zu erstellen, wird Vue.JS als Javascript-Framework eingesetzt, während Openlayers als Geospatial-Bibliothek für die Verarbeitung von Vektordaten verwendet wird.

Auf der Serverseite werden PostgreSQL und PostGIS zur Verwaltung von Geodaten verwendet, und die Conveyal-R5-Engine wird zur Durchführung von Fahrtenanalysen für den öffentlichen Verkehr eingesetzt.

Die gesamte Software, die in GOAT verwendet wird, ist Open Source und hat eine starke weltweite Akzeptanz und Reputation in der Community. 
