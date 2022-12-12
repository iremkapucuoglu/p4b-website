---
title: Technical Architecture
permalink: "/docs/technicalarchitecture/"
sections:
- about
weight: 30

---
#### System architecture

GOAT is a WebGIS-application that can be used for various formal and informal planning processes. GOAT's architecture includes a variety of software, including libraries and programming languages.

The efficient interaction of the different software in GOAT is made possible by the popular classical server-client architecture of the web. Like many other applications today, GOAT has a database that allows for efficient information storage and organization. 

As a result, information can be appropriately accessed, managed, and updated. The PostgreSQL database is used in conjunction with the PostGIS spatial extension.

As API, a Python server powered by FastAPI is used. The API serves geospatial data in different formats. Besides the GeoJSON format, compressed formats like Geobuf or Vector tiles allow for fast loading times. Besides endpoints serving spatial data, several endpoints are relevant for the application's business logic. 

<img src="\images\docs\about\server_client.webp" alt="Server-Client architecture" style="max-height:400px;"/>

The common web stack apps like HTML, CSS and JavaScript built the frontend. To create graphical user interfaces for Web applications using HTML syntax, Vue.JS is utilized as a Javascript framework, while Openlayers is used as a geospatial library for working with vector data.
 
On the server side, PostgreSQL and PostGIS are used to manage geospatial data, and the Conveyal-R5 Engine is used to perform trip analysis for public transportation.

All of the software used in GOAT is open source and has widespread acceptance and reputation in the global community.

