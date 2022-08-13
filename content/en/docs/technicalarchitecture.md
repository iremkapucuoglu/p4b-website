---
title: Technical Architecture
permalink: "/docs/technicalarchitecture/"
sections:
- about
weight: 30

---
#### System architecture

GOAT is, technically speaking, a WebGIS-application. The architecture of GOAT involves various software, including several libraries and programming languages. The efficient interaction of software in GOAT is made possible by the popular classical server-client architecture of the web. Like many applications today, GOAT has a database that allows efficient storage and organization of information. Information can therefore be accessed, managed, and updated appropriately. The PostgreSQL database is used with the spatial extension PostGIS.

![](/images/docs/about/libraries_used.webp)

As API a Python server powered by FastAPI is used. The API serves geospatial data in different formats. Besides the GeoJSON format, compressed formats like Geobuf or Vector tiles allow for fast loading times. Besides endpoints serving spatial data, several endpoints are relevant for the application's business logic. 

![](/images/docs/about/server_client_architecture.webp)

The frontend is written using the common web stack (HTML, CSS, JavaScript). As Javascript framework Vue.JS and as geospatial library Openlayers is used. All software used in GOAT is open source and has a strong worldwide community acceptance and reputation. 

