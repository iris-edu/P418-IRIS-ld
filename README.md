# P418-IRIS-ld
Describe IRIS's facility and selected datasets using project P418 json-ld schemas


## example1
This folder contains a selected information to illustrate a few P418 linked data model constructs.
- ``IRISDS_OrgServ.jsonld``
  - Top level description for IRIS Data Services. It uses the ``Organization-Service`` model
  - Includes a ``gdx:SyndicationService`` element to indicate the location of  a sitemap.xml file
  - includes a ``gdx:OutreachActivity-Training`` element to illustrate specification of an upcoming workshop
- ``sitemap.xml``
  - list of links pointing to pages containing more linked data information
- ``SEED_archive_Dat.jsonld``
  - SEED archived modeled with ``Dataset`` construct with references to station and dataselect web services
- ``IRISWS_Serv.jsonld``
  - IRIS Web Service page modeled as a ``Service``
  - Three services are modeled in two different ways, as
    - availableChannel->ServiceChannel->providesService->Service
    - serviceOutput->Services


## to deploy example 1
1) Add sitemap.xml to the web site at http://service.iris.edu/

For each of the following jsonld files, insert contents as this element in the respective html page
```html
<script type="application/ld+json">
jsonld content
</script>
```
2) Insert ``IRISDS_OrgServ.jsonld`` into page http://ds.iris.edu/ds/

3) Insert ``SEED_archive_Dat.jsonld`` into page http://service.iris.edu/fdsnws/

4) Insert ``IRISWS_Serv.jsonld`` into page http://service.iris.edu/irisws/
