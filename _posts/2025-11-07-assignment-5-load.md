---
layout: post
title:  "Assignment 5: Load"
date:   2025-11-07
assigned: 2025-11-14
due: 2025-12-12
categories: activities assignments metadata python csv collection load
canvas-link: https://umich.instructure.com/courses/779862/assignments/2943873
published: true
---

The final step of the assignment is structured around the load / ingest steps that will complete the workflow. The goal of the assignment is to create as a collection that is as complete as possible given the resources that you identified in your content group. The resources should be presented as visible and searchable in either Omeka S or CollectionBuilder (or both!).

There will be a few distinct steps here, including: preparing resource metadata for load, gathering and ingesting images, and quality control.

### Resource Metadata (CSV/JSON implementation of your MAP)

You will need to ensure that your metadata transformation workflow is implementing your map correctly. Note that you may need to work out some text formatting to correctly display the information as desired on your presentation site. If you use CSV as your ingest format, a relatively small number of changes should be required to modify your code from [Assignment 4]({% link _posts/2025-10-30-assignment-4-transform-2-implementation.md %}).

### Digital Content (Images of as many objects as possible)

One challenge of this load step will be to match and prepare images for ingest.
You will need to identify a way to match image files to the metadata records corresponding to that object, so in the presentation they will be linked together.
This should be possible by matching the object ID to the matching ID in the image file. (This may be possible using regular expressions, or alternatively using a fuzzy matching approach with a library like `fuzzywuzzy`.)

One new situation you may need to address is that multiple digital images may correspond
to one metadata record. Both Omeka S and CollectionBuilder can handle this case.
In Omeka S, you can ingest multiple files per item if you us the API,
or you can ingest images and match them individually to metadata records.
In CollectionBuilder, additional images are appended into the site data
records, without a new collection ID, [as described in the documentation for Compound Objects](https://collectionbuilder.github.io/cb-docs/docs/metadata/compound-objects/).

### Quality Control

You should have a basic way to check on your workflow's performance.
To do this, something along the lines of the "mini LOG" outputs of the transform step
would be sufficient. You should have a report that can show:
how many resources you hoped to gather (in your Extract & Transform steps),
how many resources you actually gathered (how many you plan to Load),
how many resource files you identified (in the above steps),
how many resource files were actually ingested.
This is a rough estimate, but can be a helpful indicator you can
use to improve the workflow, or to provide a confirmation that the process was successful.

## Deliverables

1. The CSV or JSON file(s) that you use to load resources to your site.
2. The link to the site with metadata and resources loaded.
3. A quality control report (should be a text file or table, CSV or Excel).

### Resources

- [Assignment submission on Canvas]({{ page.canvas-link }})
