---
title: Walkability Index
permalink: "/docs/walkability_index/"
sections:
- technical
weight: 80

---
Within the project [WALKIE](../../posts/2021-04-06-walkability-index/), we developed a Walkability Index that shows how attractive paths are for pedestrians. This index can be used to identify shortcoming in the local walking path network.

The Walkability Index consists of 22 items, that are clustered in 6 categories:

![Items and weights of the Walkability Index](/images/docs/technical_documentation/walkability_index/indicators_en.webp "Walkability indicators and weighting factors")

The weighting of the items is done based on several scientific studies (references listed below) and according to the data availability. For some items (e.g. sidewalk width), data availability in Open Data sources (such as OSM) is very limited. Therefore, these items are excluded from the index calculation.

Also after omitting these items, not all the information to be included in the index is available for all paths. If information is missing for one item or a whole category, it is therefore omitted and the other items or categories are given a higher weight.

### References

Ivan Blečić, Arnaldo Cecchini, Tanja Congiu, Giovanna Fancello & Giuseppe A. Trunfio (2015) Evaluating walkability: a capability-wise planning and design support system. International Journal of Geographical Information Science. 29:8. 1350-1374. DOI: 10.1080/13658816.2015.1026824

Lorraine Fitzsimons D'Arcy (2013) A multidisciplinary examination of walkability: Its concept, measurement and applicability. PhD thesis. Dublin City University.

Spittaels, H., Foster, C., Oppert, JM. et al. Assessment of environmental correlates of physical activity: development of a European questionnaire. Int J Behav Nutr Phys Act 6, 39 (2009). https://doi.org/10.1186/1479-5868-6-39

Vale, D. S., Saraiva, M., & Pereira, M. (2015). Active accessibility: A review of operational measures of walking and cycling accessibility. Journal of Transport and Land Use, 9(1). https://doi.org/10.5198/jtlu.2015.593

Kevin Manaugh, Ahmed El-Geneidy. (2011) Validating walkability indices: How do different households respond to the walkability of their neighborhood? Transportation Research Part D: Transport and Environment. Volume 16. Issue 4. Pages 309-315. ISSN 1361-9209. https://doi.org/10.1016/j.trd.2011.01.009.