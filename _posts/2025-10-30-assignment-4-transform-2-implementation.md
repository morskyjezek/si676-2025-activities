---
layout: post
title:  "Assignment 4: Transform 2 Implementing Your MAP"
date:   2025-10-30
assigned: 2025-10-31
due: 2025-11-21
categories: activities assignments metadata transformation python
canvas-link: https://umich.instructure.com/courses/779862/assignments/2877247
published: true
---

The goal of this assignment is to implement the metadata transformation that was implied in your MAP document ([Assignment 3]({% link _posts/2025-10-20-assignment-3-transform-1-map-planning.md %})). Your task is to develop a batch workflow (script based) that will transform from the origin data (in this case the UMMAA spreadsheet), apply the rules for destination fields and formatting, then transform it to a format that you can ingest into Omeka S or CollectionBuilder. It's possible that you need to make some modifications by hand, but to the extent possible your script tools should automate as much of this process as possible so that the contents display in the new platforms as clearly and accurately as possible. The deliverables for this assignment are the Python script that accomplishes the transformation and the resulting CSV, JSON, or other files that your workflow generates. At this point, you will have all of the steps needed for importing the objects successfully into your site. In other words, your script(s) will pull data from the original metadata, transform that data, and you will be ready to batch upload the objects from a CSV or API.

Omeka S Tip: create an item set for the new set, which will make it easier to identify the materials from a specific import batch.  

## Deliverables

1. The script(s) that extracts & transforms the original data from UMMAA. For this part, you can turn in a `.py` or `.ipynb`.
2. The script outputs (that is, the transformed data likely in CSV or JSON).

### Resources

- [Assignment submission on Canvas]({{ page.canvas-link }})
- [Sample MAP Implementation, JSON to CSV (Jupyter notebook)][sample-map-implementation-ipynb]

[sample-map-implementation-ipynb]: https://github.com/morskyjezek/si676-2025-data/blob/main/examples/assignment-transform-2-json-to-csv.ipynb
