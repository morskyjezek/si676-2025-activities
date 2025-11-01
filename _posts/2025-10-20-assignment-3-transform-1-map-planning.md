---
layout: post
title:  "Assignment 3: Transform 1 Designing a MAP"
date:   2025-10-20
assigned: 2025-10-31
due: 2025-11-17
categories: activities assignments metadata map
canvas-link: https://umich.instructure.com/courses/779862/assignments/2877246
published: false
---

For this assignment, each team is tasked with designing a MAP for the UMMAA items you're working on. These will likely be similar, but each team should develop their own. Start by working with the fields associated with your object type in the [large metadata spreadsheet](https://www.dropbox.com/scl/fi/l9ej5ssttmeraagx13hgj/UMMAA_all_Philippine_objects-for_distribution.xlsx?rlkey=zy7dku758a9xgku677pdgq5im&amp;st=1g6c5ki1&amp;dl=0).

## Metadata Profiles

A metadata application profile (MAP). This is a technical document that will express all of the types of items and the descriptive information about them that you plan to collect. It will note where they come from (in most cases, these descriptions will be from already extant schemas), how they are used, what is valid or invalid, whether they are required or not required, and whether they are repeatable.

It is often important to model your metadata when deciding which fields are necessary and how to use them. In this case, we are skirting that step since we are reusing already-created metadata. **It is, however, useful to have a record of what metadata you are choosing, whether it comes form another extant scheme, and how you are using each field.** In the context of this exercise, the purpose is clear: document the kinds of metadata that already appear for the files in your repository. The key is to identify which types of information are used, their granularity, and their relationship to the items as well as more broadly to the collection (that is, can likely be expressed in a generic DublinCore profile). (Additional, but more conceptual, guidelines for Dublin Core Application Profiles at at [link to DublinCore application profile guidelines](https://www.dublincore.org/specifications/dublin-core/profile-guidelines/).

## Metadata crosswalking resources

<ul>
    <li aria-level="1"><span>Mary S. Woodley, &ldquo;Metadata Matters: Connecting People and Information,&rdquo; in </span><i><span>Introduction to Metadata</span></i><span>, ed. and rev. Murtha Baca, 3rd edition (Getty Publications, 2016), available at </span><a href="https://www.getty.edu/publications/intrometadata/metadata-matters/" data-verified-link="true"><span>https://www.getty.edu/publications/intrometadata/metadata-matters/</span></a><span>.&nbsp;&nbsp;</span></li>
    <li aria-level="1"><span>Digital Library Federation Metadata Application Profile Clearinghouse, available at </span><a href="https://dlfmetadataassessment.github.io/MetadataSpecsClearinghouse/" data-verified-link="true"><span>https://dlfmetadataassessment.github.io/MetadataSpecsClearinghouse/</span></a><span>&nbsp;</span></li>
    <li aria-level="1"><span>Dublin Core Metadata Initiative (DCMI), &ldquo;DC Tabular Application Profiles,&rdquo; ed. Karen Coyle, online at </span><a href="https://www.dublincore.org/groups/application-profiles/dctap-primer/" data-verified-link="true"><span>https://www.dublincore.org/groups/application-profiles/dctap-primer/</span></a><span>.&nbsp;&nbsp;</span></li>
</ul>

## Examples / Templates

You can find some examples of MAPs at [link to the DLF's MAP "clearinghouse" project](https://dlfmetadataassessment.github.io/MetadataSpecsClearinghouse/).

<ul>
    <li>For example, the PA Digital Metadata Guidelines 1.2 is a very clear example: <a href="https://dlfmetadataassessment.github.io/assets/maps/PA_Digital_Metadata_Guidelines-v1.2(August_2018).pdf" target="_blank" rel="noopener">https://dlfmetadataassessment.github.io/assets/maps/PA_Digital_Metadata_Guidelines-v1.2(August_2018).pdf</a>.&nbsp;</li>
    <li>Likewise, the Empire State Digital Network Metadata Guidelines: <a href="https://dlfmetadataassessment.github.io/assets/maps/ESDN_Metadata_Best_Practices_and_Guidelines.pdf" target="_blank" rel="noopener">https://dlfmetadataassessment.github.io/assets/maps/ESDN_Metadata_Best_Practices_and_Guidelines.pdf</a>.&nbsp;&nbsp;</li>
    <li>Another variation is the TAP, which is intended to be computer processable, which encodes everything as a CSV table, with appropriate namespace prefixes. This is under development by the DCMI TAP project, which provides a useful primer on how to think about this: <a href="https://github.com/dcmi/dctap/blob/main/TAPprimer.md" target="_blank" rel="noopener">https://github.com/dcmi/dctap/blob/main/TAPprimer.md</a>. This resource is particularly useful in demonstrating how this information may be placed into a data table, which will be useful for making an actionable crosswalk (the next assignment).&nbsp;</li>
</ul>

Please model your MAP after one of the above examples.

## What to Submit

1. **Your MAP.** It should have an introductory statement explaining what it is, an alphabetical list of all the terms described (alphabetize by term name), a key (the fields explained for each term), and then each term listed out individually as a table (or row if you are using the TAP variation). Each term table describes the basic rules governing the term's use, and equivalence/relationship in DC (crosswalk), which applies to your Omeka site. Begin with the list of terms that you pull from loc.gov and directions on how to crosswalk them into the scheme that you are using in your Omeka S site. Each term table should state what standards the term comes from (DC, MODS, or other). Explain how you are using each term: is it applied at the collection or item level, repeatable, what conventions do you use to transcribe the information, are they human created by hand or created automatically? Etc. Essentially, begin with a table of terms that you extract from the loc.gov collection, direct equivalents in at least two other metadata schemes (suggested are mostly DublinCore but possibly also MODS, and you can consider others if you like), and notes on why you chose the target field, considerations (like information that may be lost), and any conventions on data encoding. For a sample, [see the table in the pulling data Jupyter notebook in the course GitHub repo](https://github.com/morskyjezek/si676-2025-data/blob/main/examples/assignment-transform-1-design-metadata-profile.ipynb). Include at least 15 fields in your index and 15 corresponding tables for each term.
2. **A short reflection on this process (300-500 words).** How did you find the process of extracting the collection information from loc.gov? What did you learn about crosswalking the information into the fields that you have in your Omeka site? Although both the source and your target site should be using standards, did you find the process to be subjective? What sorts of decisions did you make when developing the crosswalk?

### Resources

- [Assignment submission on Canvas]({{ page.canvas-link }})
- [Sample MAP Planning (Jupyter notebook)][sample-map-planner-ipynb]
- [Sample MAP Planning (Google Sheet used in class)][sample-map-planner-sheets] - if useful, make a copy to use for your project!

[sample-map-planner-ipynb]: https://github.com/morskyjezek/si676-2025-data/blob/main/examples/assignment-transform-1-design-metadata-profile.ipynb
[sample-map-planner-sheets]: https://docs.google.com/spreadsheets/d/1L70qpywZXRxzsS_2JOg9cMCALJPu2yfDLxV7lq43QDI/edit?gid=0#gid=0
