---
title: ÖV Güteklassen
permalink: /en/docs/oev_gueteklasse/
lang: en
sections:
- technical
weight: 40
---

The quality of accessibility is a decisive indicator in public transport and spatial planning. It can be used to highlight deficits in accessibility and to identify well-serviced locations as attractive areas for development. The approach of public transport quality classes (German: _ÖV Güteklassen_) is methodologically superior compared to common catchment radii. In 2011, the Swiss Federal Office for Spatial Development (ARE) used the indicator of public transport quality classes in order to include the attractiveness of public transport services in the assessment of development quality; since then, these have been considered an important instrument in formal planning processes in Switzerland. In addition, the Swiss model served as an inspiration for application in Austria (e.g. Voralberg).  

The institutionalisation of the indicator in German-speaking countries, as well as the comprehensible and at the same time differentiated calculation methodology, are important advantages of the public transport quality classes. For use in GOAT, the indicator was adapted to the conditions in Germany. At the same time, the calculation period was made more flexible so that the indicator can be calculated for any day of the week and time of day. In the Swiss version of the indicator, the calculation of the quality classes is usually carried out for departures on weekdays between 6-20 hrs. The calculation methodology implemented in GOAT is explained in more detail below.  

![Classification of transport stops](/images/docs/oev_gueteklasse/classification_stations_en.webp "Classification of transport stops")

The calculations are carried out on the basis of GTFS data. First, the number of departures per public transport mode (underground, tram, bus and train) is dynamically calculated for each station. The sum of the departures is divided by two to calculate the frequency, in order to eliminate the outward and return directions. In the next step, the average frequency for the selected time interval is calculated. The higher-value service is selected as the station type in the case of service by several means of transport. For example, in the case of bus and train, this is the train. With the help of the table above, as well as the station type and the frequency, the station category can now be determined. 

![Determination of public transport quality classes](/images/docs/oev_gueteklasse/determination_oev_gueteklasse_en.webp "Determination of public transport quality classes")

Subsequently, radii of the size shown are calculated for the corresponding station categories. This creates several radii that are merged. For overlapping radii, the higher quality class is used. 

# References

Bundesamt für Raumentwicklung ARE, 2022. ÖV-Güteklassen Berechnungsmethodik ARE (Grundlagenbericht).

metron, 2017. Bedienungsqualität und Erschließungsgüte im Öffentlichen Verkehr.

Hiess, H., 2017. Entwicklung eines Umsetzungskonzeptes für österreichweite ÖV-Güteklassen.
