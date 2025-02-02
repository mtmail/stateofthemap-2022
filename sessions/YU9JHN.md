---
doi: "10.5281/zenodo.7004483"
layout: session_academic
title: "Comparative Integration Potential Analyses of OSM and Wikidata – the Case Study of Railway Stations"
code: "YU9JHN"
speaker_names: [
  'Alishiba Dsouza (Data Science & Intelligent Systems, University of Bonn, Germany)',
  'Moritz Schott (Institute of Geography, GIScience, Heidelberg University, Germany)',
  'Sven Lautenbach (Institute of Geography, GIScience, Heidelberg University, Germany)'
]
affiliations: None
room: "Auditorium B"
length: "20"
time: "Sunday, 10:00"
time_iso: "2022-08-21T08:00:00Z"
resources: [{ description: "Presentation", url: "/attachments/YU9JHN_Comparative_Wikidata_D_QErzpl1.pdf" }]
recording: True
---

In this work, we present analyses using a series of comparative data insights that help to better understand the potential and implications of integration between knowledge graphs and OSM.

<hr>

OpenStreetMap(OSM) is one of the richest and most diverse sources of geographic information. However, it lacks a fundamental property vital for spatio-semantic analyses: hierarchical structure and semantic linkage. OSM provides links to existing knowledge graphs (structured data that conforms to a specific ontology) e.g., via the wikidata=* tags. The usage of these link-tags is currently limited to a small percentage of both OSM and Wikidata objects. Efforts were undertaken to enhance the geographic linking, linking nearby objects of the same type and semantic linking [1-3]. On the side of the hierarchical and semantic structuring of OSM, the WorldKG knowledge graph[4] provides a semantic mapping of a large subset of OSM. While the free and open OSM tagging scheme is a fundamental part of the OSM project that enabled its success, WorldKG overcomes the inherent lack of structure this tagging scheme represents, paving the way for a knowledge-graph integration of the OSM dataset. Still, open knowledge graphs and OSM are not fully integrated. 

The following analyses provide a series of comparative data insights that help to better understand the potential and implications of integration between knowledge graphs and OSM. In this work, OSM is compared to Wikidata, one of the largest open knowledge graph projects from the Wikimedia Foundation that provides structured storage to other Wikimedia projects such as Wikipedia. Wikidata can, in many aspects, be compared to OSM by its community structure, its free and open nature, and simple contribution framework. In this work, the two datasets are first compared in size, data structure, and distribution. Later, we extend our analyses with a community comparison. The presented analyses also examine how two separate online communities with similar interests have evolved.    

Grasping the size of the two projects is a straightforward task and visible on their websites: OSM features around 1 billion elements [5], while Wikidata is much smaller with over 97 million objects, of which approximately 9 million have geographic coordinates. The topic of railway stations was chosen because these objects have a comparable definition and are well represented in both datasets with ca. 130k and 100k elements in OSM and Wikidata, respectively, indicating integration potential. In OSM, railway stations are mapped by the tags 'railway=station' or 'railway=halt'. In Wikidata, the 'instance of (P31)' property containing 'Q55488' value represents Railway Station (object type).    

By defining generalizable comparison indicators, the presented work provides a framework and source code (available at https://gitlab.gistools.geog.uni-heidelberg.de/giscience/ideal-vgi/osm-wikidata-comparison under the GNU Affero General Public License v3) for VGI project description, comparison, and monitoring. Similar approaches have been established for OSM contributors [6], for single OSM elements [7], and for small geographic regions [8]. For data collection in Wikidata, Wikidata API (https://www.wikidata.org/w/api.php) and Wikidata SPARQL endpoint were used. For Wikidata objects mapped with 'Railway Station', their revision history containing user information, timestamps, and a number of properties was collected. Overall contributions were collected from all users who have contributed to at least one object typed 'Railway Station'. OSM data collection was done using the ohsome API (https://ohsome.org) to extract all railway stations mapped in OSM, including their history and all edits made by the users who edited these railway stations. In addition to a general comparison between the datasets, we derived five sets for a more detailed comparison: OSM with links to Wikidata (59,441 elements), OSM without links to Wikidata (74,659), Wikidata that have links from OSM and are typed as railway stations (45,050), Wikidata without links to OSM but with geocoordinates (54,594) and Wikidata without links to OSM and without geocoordinates (6,714).   

Our first analysis regarding the growth rate of the two sources showed that OSM has reached a saturated state regarding the number of railway stations, where only a few stations were added since mid-2020. Wikidata, on the other hand, still experiences a stable number of new stations that are added to the project. The two datasets depict no clear temporal correlation hinting towards two independent communities, meaning that edits in OSM are not followed by edits in Wikidata and vice versa. Despite the similar size of the two datasets at a global scale, the two datasets show significant discrepancies on a country level. For example, in China, Wikidata features only 39% of the stations present in OSM while having more than double the amount of stations in the United Kingdom. While the lack of stations seems reasonable considering the overall lack of stations in Wikidata, the overabundance of stations in the UK hints towards a data issue that needs more detailed analyses before integration.  
In terms of properties/tags of each object, we observed that Wikidata has, on average more properties per object than OSM. Since Wikidata is a knowledge graph, it also contains links to other objects that can help enrich existing objects increasing this discrepancy even further. OSM objects with links to Wikidatda have almost double the tags compared to those without links. This could either be a quality indicator or an indicator that only famous stations, which are very well mapped in OSM, are also linked to Wikidata. Wikidata objects without links from OSM and geocoordinates have the least number of properties, hinting at their lower quality.    

Next, we present the community analysis. There were around 8.4 million contributors in OSM in total, and 48k unique users have contributed to either creation, deletion, or updating of the railway station objects. In Wikidata, the number of overall contributors is much smaller, i.e., 24k out of which 14k have contributed to Railway objects. The revisions for Wikidata objects are around 11 times higher than that of OSM revisions. This is evident as Wikidata railway stations have more properties than OSM railway stations. This could also be because OSM contributors have a wide variety of objects to map, whether a bench or a tree. In contrast, Wikidata contributors may focus on details and enrichment of prominent objects of public interest. In OSM, adding a new object to the map may take priority over extensive tagging of existing objects. A similar trend is observed for average stations created by each contributor wherein, on average, Wikidata contributors have created five times and, with median statistics, two times more objects than OSM contributors. This may be due to the higher number of bots and imports in Wikidata. While OSM users generally map a specific area that can only feature a limited number of railway stations, Wikidata users may import railway stations from other sources without limiting themselves to a certain geographical unit.   

To conclude, we notice that both communities have great potential to integrate these sources on the topic of railway stations. This potential increases daily with other topics reaching a mature data state in Wikidata and other knowledge graphs. OSM can benefit from the wide range of semantic information linked to objects, while Wikidata can benefit from the precise geoinformation and completeness OSM offers. Yet, care needs to be taken to take both communities on board as each user base exhibits unique data collection styles that need to be respected.

<hr>

[1] Tempelmeier, N., &amp; Demidova, E. (2021). Linking OpenStreetMap with knowledge graphs—Link discovery for schema-agnostic volunteered geographic information. Future Generation Computer Systems, 116, 349-364. 

[2] Dsouza, A., Tempelmeier, N., &amp; Demidova, E. (2021, October). Towards Neural Schema Alignment for OpenStreetMap and Knowledge Graphs. In International Semantic Web Conference (pp. 56-73). Springer, Cham. 

[3] Gurtovoy, D., &amp; Gottschalk, S. (2022). Linking Streets in OpenStreetMap to Persons in Wikidata., In WWW ’22 Companion. 

[4] Dsouza, A., Tempelmeier, N., Yu, R., Gottschalk, S., &amp; Demidova, E. (2021, October). WorldKG: A World-Scale Geographic Knowledge Graph. In Proceedings of the 30th ACM International Conference on Information &amp; Knowledge Management (pp. 4475-4484). 

[5] Schott, M., Herfort, B., Troilo, R., &amp; Raifer, M. (2022, January 20). A basic guide to OSM data filtering. [web log]. Retrieved May 19, 2022, from http://k1z.blog.uni-heidelberg.de/2022/01/20/a-basic-guide-to-osm-data-filtering/  

[6] Schott, M., Grinberger, A. Y., Lautenbach, S., &amp; Zipf, A. (2021). The Impact of Community Happenings in OpenStreetMap—Establishing a Framework for Online Community Member Activity Analyses. ISPRS International Journal of Geo-Information, 10(3), 164. 

[7] Schott, M., Größchen, L., &amp; Lautenbach, S. (2022, April 20). Version (0.1). OSM Element Vectorisation. Retrieved May 19, 2022, from https://gitlab.gistools.geog.uni-heidelberg.de/giscience/ideal-vgi/osm-element-vectorisation.  

[8] ohsome Team. (2022, April 12). Version (0.9.0). ohsome quality analyst. Retrieved May 19, 2022, from https://github.com/GIScience/ohsome-quality-analyst.

