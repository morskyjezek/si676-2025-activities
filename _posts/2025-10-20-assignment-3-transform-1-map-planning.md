---
layout: post
title:  "Assignment 3: Transform 1 Designing a MAP"
date:   2025-10-20
assigned: 2025-10-31
due: 2025-11-17
categories: activities assignments metadata map
canvas-link: https://umich.instructure.com/courses/779862/assignments/2877246
published: true
---

A **metadata application profile (MAP)** is a technical document that documents and expresses all of the types of items and the descriptive information about them that you plan to collect. It documents whe the information comes from (in most cases, these descriptions will be from already extant schemas), how they are used in your local site, what is valid or invalid, whether they are required or not required, and whether they are repeatable.

## Assignment Background and Resources

For this assignment, each team is tasked with designing a MAP for a set of objects from the [University of Michigan Museum of Anthropological Archaeology (UMMAA)](https://lsa.umich.edu/ummaa). These objects are selected from the University's various collections relating to the Philippines. More [information about the collections has been assembled by the ReConnect/ReCollect project](https://www.reconnect-recollect.com/the-philippine-collections/). Their website offers a useful overview, and if you are interested in learning more about why these collections are at the university and the conditions under which they were collected, I recommend watching Professor Deirdre de la Cruz's talk for the Making Michigan series, ["A Difficult Archive" (October 13, 2022)](https://www.youtube.com/watch?v=dbGdvxvV4r0). An additioanl resource is the UMMAA's current curated presentation of selected objects from the collection, found at [Philippine Collections UMMAA](https://sites.lsa.umich.edu/ummaa-philippines/).

The bulk of the work is in modeling the metadata you're receiving, then deciding how these fields are will be used in your new site. Your task is to: document the kinds of metadata that already appear in the data from the museum, then plan where they go in your digital repository site. The key is to identify which types of information are used, their granularity, and their relationship to the items as well as more broadly to the collection (that is, can likely be expressed in a generic DublinCore profile). (Additional, but more conceptual, guidelines for designing DublinCore Application Profiles are at [link to DublinCore application profile guidelines](https://www.dublincore.org/specifications/dublin-core/profile-guidelines/).)

Each group's MAP will likely be similar, but each team should develop their own. Start by working with the fields associated with your object type in the [large metadata spreadsheet](https://www.dropbox.com/scl/fi/l9ej5ssttmeraagx13hgj/UMMAA_all_Philippine_objects-for_distribution.xlsx?rlkey=zy7dku758a9xgku677pdgq5im&st=1g6c5ki1&dl=0).

The large metadata sheet linked above should have data about all of the objects in the Philippine collections. Each group is tasked with a specific subset of objects, specified by obejct type. Use the following table to link to the objects for each type:

| Group Name           | Objects Folder |
| ------ | ------ |
| Baskets              | [Dropbox folder](https://www.dropbox.com/scl/fo/zdccuo6h0w5219bdak6kj/AFaVZNWTJx7vinCwWCtGovA?rlkey=m0f3zsgmq5oiogc7zbctjtkvd&st=uk2dri6r&dl=0) (requires same password as above) |
| Ethnographic Objects | [Dropbox folder](https://www.dropbox.com/scl/fo/zkje8i46nbniq73ohc0va/ABkfBybLu-A5dBGEu0Pvi3k?rlkey=hw3dvwm7f3gwjgo764npkf9ar&st=qiduopev&dl=0) (requires same password as above) |
| Textiles             | [Dropbox folder](https://www.dropbox.com/scl/fo/v65i3gpq12doz6soujnj7/AL_gY7wZbuO-dnjffwmXtAE?rlkey=7vg1ltodurlxy4tbn9t45159t&st=vb4afp2e&dl=0) (requires same password as above) |

You can access [all of the digitized object files and data in this dropbox folder](https://www.dropbox.com/scl/fo/wuegxdc1a8ptzgyrz3a40/AFTTxYdJ-PYwPyyBdlWxQk8?rlkey=vgosvxx14crnrd9fwio7i351g&st=8k3fx7fl&dl=0) (U-M login may be required).

Questions will undoubtedly arise as you are working with the data. Because we can be in touch with the data creators (a luxury that is not always possible!), please [note your questions about the data in this shared doc](https://docs.google.com/document/d/1J7vB2i2CcuB8B0JZD9eDlSy2kp8LUcdQ-KD3Iw4N-YY/edit?usp=sharing), so they can be grouped and shared to the UMMAA collection managers.

## Researching metadata schemes

To the extent possible, your destination fields should come from standardized (or at least known) extant metadata schemes. A large majority of these can come from DublinCore, but you will find that DublinCore does not have the granularity to accurately describe all of the terms in the museum data. You should therefore investigate fields from at least one other scheme.

Here are some additional schemes to consider, with links to their description and documentation:

- [DublinCore Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/) ([Wikipedia](https://en.wikipedia.org/wiki/Dublin_Core))
- [MODS](http://www.loc.gov/standards/mods/) ([Metadata Standards Catalog entry](https://rdamsc.bath.ac.uk/msc/m97), Wikipedia)
- [CIDOC CRM](https://cidoc-crm.org/), leading object-focused Conceptual Reference Model maintained by the International Council on Museums ([eCRM OWL file](https://github.com/erlangen-crm/ecrm/blob/master/ecrm_current.owl), [wikipedia article](https://en.wikipedia.org/wiki/CIDOC_Conceptual_Reference_Model))
- [LIDO](https://cidoc.mini.icom.museum/working-groups/lido/lido-overview/lido-schema/) (Metadata Standards Catalog, [Wikipedia](https://en.wikipedia.org/wiki/LIDO))
- [CCO (Cataloging Cultural Objects)](https://www.vraweb.org/cco) ([Wikipedia](https://en.wikipedia.org/wiki/Visual_Resources_Association#Cataloguing_Cultural_Objects_(CCO)))

An additional resource that may be of use in researching schemes and other metadata fields
is the [Linked Open Vocabularies (LOV) database](https://lov.linkeddata.es/dataset/lov),
which provides a search interface for metadata schemes,
but also provides the capacity to search across term/field names. This does not include all
schemes, but it does include most that are used in cultural heritage and are also represented
in a formal schema definition or ontology. The term search can be found directly at <https://lov.linkeddata.es/dataset/lov/terms>.

## Metadata crosswalking resources

- Mary S. Woodley, “Metadata Matters: Connecting People and Information,” in _Introduction to Metadata_, ed. and rev. Murtha Baca, 3rd edition (Getty Publications, 2016), available at [https://www.getty.edu/publications/intrometadata/metadata-matters/](https://www.getty.edu/publications/intrometadata/metadata-matters/).  
- Digital Library Federation Metadata Application Profile Clearinghouse, available at [https://dlfmetadataassessment.github.io/MetadataSpecsClearinghouse/](https://dlfmetadataassessment.github.io/MetadataSpecsClearinghouse/)
- Dublin Core Metadata Initiative (DCMI), “DC Tabular Application Profiles,” ed. Karen Coyle, online at [https://www.dublincore.org/groups/application-profiles/dctap-primer/](https://www.dublincore.org/groups/application-profiles/dctap-primer/) 

## MAP Examples / Templates

You can find some examples of MAPs at [link to the DLF's MAP "clearinghouse" project](https://dlfmetadataassessment.github.io/MetadataSpecsClearinghouse/).

- For example, the PA Digital Metadata Guidelines 1.2 is a very clear example: [https://dlfmetadataassessment.github.io/assets/maps/PA\_Digital\_Metadata\_Guidelines-v1.2(August\_2018).pdf](https://dlfmetadataassessment.github.io/assets/maps/PA_Digital_Metadata_Guidelines-v1.2(August_2018).pdf).
- Likewise, the Empire State Digital Network Metadata Guidelines: [https://dlfmetadataassessment.github.io/assets/maps/ESDN\_Metadata\_Best\_Practices\_and\_Guidelines.pdf](https://dlfmetadataassessment.github.io/assets/maps/ESDN_Metadata_Best_Practices_and_Guidelines.pdf).  
- Another variation is the TAP, which is intended to be computer processable, which encodes everything as a CSV table, with appropriate namespace prefixes. This is under development by the DCMI TAP project, which provides a useful primer on how to think about this: [https://github.com/dcmi/dctap/blob/main/TAPprimer.md](https://github.com/dcmi/dctap/blob/main/TAPprimer.md). This resource is particularly useful in demonstrating how this information may be placed into a data table, which will be useful for making an actionable crosswalk (the next assignment).

Please model your MAP after one of the above examples.

## What to Submit

1. **Your MAP.** It should have an introductory statement explaining what it is, an alphabetical list of all the terms described (alphabetize by term name), a key (the fields explained for each term), and then each term listed out individually as a table (or row if you are using the TAP variation). Each term table describes the basic rules governing the term's use, and equivalence/relationship in DC (crosswalk), which applies to your Omeka site. Begin with the list of terms that you pull from loc.gov and directions on how to crosswalk them into the scheme that you are using in your Omeka S site. Each term table should state what standards the term comes from (DC, MODS, or other). Explain how you are using each term: is it applied at the collection or item level, repeatable, what conventions do you use to transcribe the information, are they human created by hand or created automatically? Etc. Essentially, begin with a table of terms that you extract from the loc.gov collection, direct equivalents in at least two other metadata schemes (suggested are mostly DublinCore but possibly also MODS, and you can consider others if you like), and notes on why you chose the target field, considerations (like information that may be lost), and any conventions on data encoding. For a sample, see the table in the pulling data Jupyter notebook in the course GitHub repo ([link here](https://github.com/morskyjezek/si676-2025-data/blob/main/examples/assignment-transform-1-design-metadata-profile.ipynb)). Include at least 15 fields in your index and 15 corresponding tables for each term.
2. **A short reflection on this process (300-500 words).** How did you find the process of extracting the collection information from loc.gov? What did you learn about crosswalking the information into the fields that you have in your Omeka site? Although both the source and your target site should be using standards, did you find the process to be subjective? What sorts of decisions did you make when developing the crosswalk?

### Resources

- [Assignment submission on Canvas]({{ page.canvas-link }})
- [Sample MAP Planning (Jupyter notebook)][sample-map-planner-ipynb]
- [Sample MAP Planning (Google Sheet used in class)][sample-map-planner-sheets] - if useful, make a copy to use for your project!

[sample-map-planner-ipynb]: https://github.com/morskyjezek/si676-2025-data/blob/main/examples/assignment-transform-1-design-metadata-profile.ipynb
[sample-map-planner-sheets]: https://docs.google.com/spreadsheets/d/1L70qpywZXRxzsS_2JOg9cMCALJPu2yfDLxV7lq43QDI/edit?gid=0#gid=0
