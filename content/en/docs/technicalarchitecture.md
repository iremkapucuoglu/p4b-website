---
title: Technical Architecture
permalink: "/docs/technicalarchitecture/"
sections:
- about
weight: 30

---
#### System architecture

GOAT is a WebGIS application created with open source programming languages and libraries. It follows the traditional server-client architecture utilized by web applications. This versatile tool can be applied to a variety of planning functions and processes.

![GOAT Server-Client-Architecture](/images/docs/about/server-client-architecture.webp "Server-Client-Architecture")

The foundation of GOAT's functionality is its spatially enabled database, which can store both large spatial and non-spatial data sets. A robust relational database is essential for efficient data management, storage, and processing. Therefore, GOAT relies on PostgreSQL and PostGIS, which are both widely-used mature technologies.

GOAT uses a Python server powered by FastAPI as its API. This server computes and serves business logic and various indicators in many formats, making it highly versatile. While the majority of endpoints serve data as JSON, specialized geospatial formats like Geobuf (e.g., for heatmaps), custom binary formats (e.g., for isochrones), and vector tiles (e.g., for static layers) are also available. Notably, GOAT supports further geoservices such as WMS and WFS, which comply with OGC standards and can readily integrate into the platform.

Routing functionalities are essential to the backend of GOAT, as they are used to calculate travel times for accessibility indicators. For walking and cycling, GOAT implements a custom Dijkstra algorithm while for public transport and car routing, the Conveyal R5 routing engine is used. This routing engine is intermodal in nature and combines street networks with timetable data, making it a powerful tool for producing realistic travel times.

The frontend is build in Javascript using the Vue.js framework. To provide geospatial capabilities the Openlayers library is used. The frontend communicates with the backend by requesting and sending data to the API. Meanwhile, the frontend has rich capabilities to display and interact with the data. All of the software used in GOAT is open source and has widespread acceptance and reputation in the global community. 

For the deployment Kubernetes is used. Kubernetes is an open-source system for automating deployment, scaling, and management of containerized applications. It groups containers that make up an application into logical units for easy management and scalability. Kubernetes is a portable, extensible, open-source platform for managing containerized workloads and services in a vendor-neutral way. 


