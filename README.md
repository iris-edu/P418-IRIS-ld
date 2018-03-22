# P418-IRIS-ld
Examples which describe IRIS's facility and selected datasets using project P418 json-ld schemas


## example2
#### Description
- ``IRIS_DS_Organization_Service.jsonld``
  - Describes IRIS Products using ``hasOfferCatalog``
  - As examples, specifies associations for geodex ``ResearchResourceTypes`` and ``OutreachActivity-UserWorkshop``

## example1
#### Description
This folder contains a selected information to illustrate a few P418 linked data model constructs.
- ``IRIS_DS_Organization_Service.jsonld``
  - Top level description for IRIS Data Services. It uses the ``Organization-Service`` model
  - Includes additionalType ``gdx:SyndicationService`` to indicate the location of  a sitemap.xml file
  - includes additionalType ``gdx:OutreachActivity-Training`` to illustrate specification of an upcoming workshop
- ``sitemap.xml``
  - list of links pointing to pages containing more linked data information
- ``SEED_Dataset.jsonld``
  - SEED archived modeled with ``Dataset`` construct with references to Station and Dataselect web services
- ``IRIS_WS_Service.jsonld``
  - IRIS Web Service page modeled as a ``Service``
  - Three services are modeled in two different ways, as
    - availableChannel->ServiceChannel->providesService->Service
    - serviceOutput->Services


#### to deploy example 1
1) Add sitemap.xml to the web site at http://service.iris.edu/

For each of the following jsonld files, insert contents as this element in the respective html page
```html
<script type="application/ld+json">
jsonld content
</script>
```
2) Insert ``IRIS_DS_Organization_Service.jsonld`` into page http://ds.iris.edu/ds/

3) Insert ``SEED_Dataset.jsonld`` into page http://service.iris.edu/fdsnws/

4) Insert ``IRIS_WS_Service.jsonld`` into page http://service.iris.edu/irisws/
