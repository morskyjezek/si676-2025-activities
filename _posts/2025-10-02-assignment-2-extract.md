---
layout: post
title:  "Assignment 2: Extract Collection Data"
date:   2025-09-26
assigned: 2025-10-02
due: 2025-10-31
categories: activities assignments python
canvas-link: https://umich.instructure.com/courses/779862/assignments/2877243
published: true
---

In this step of the course project to build multiple collections platforms,
you are working to *extract* data for your collection sites.
this is the first step in building up a generic workflow that could
be described as *extract, transform, load*, or *ETL*.
This assignment is the step when you will collect, or "extract", that data
from another source. The next step will be to prepare, or "transform"
the data into a format that is possible for your collection site to ingest.
In later steps, you will make final configurations of your sites,
transform the data, and ingest, or "load" the content into your new sites.

## Extract Collection Data

### 1. Get collection list

The first step is to get a collection list. This is a basic
step that is the basis for your later inventory, file checking,
and checking and confirming metadata for your collection objects.

Your task is to gather information about the items in the
Library of Congress' "Free to Use Libraries" set, which is
listed at [https://www.loc.gov/free-to-use/libraries/](https://www.loc.gov/free-to-use/libraries/).
On this page, which describes the set, examine this set.
You should have a basic understanding, like how many images are there and
what kind of information you will be looking for. 

Next, look for the JSON representation of the set (remember the `fo=json` parameter).
Using Python + `requests`, request the set JSON and save it locally.
You can use whatever approach to work with Python that you are most comfortable with,
but I would suggest creating a function to do this.
This step should end with a locally saved JSON file with the information about the set.

Finally, examine the JSON representation of the set.
Within the JSON file, you need to find the `items` key;
once you locate this information, identify how many items are in the set,
and save the `image`, `link`, and `title` values for each item
to a new CSV file titled `ftu-libraries-set-list.csv`.
You will use this file as a reference for your collection list.
(If you want to see how this might look, here's a sample version: [Sample Collection List CSV file][sample-collection-list-csv] - GitHub will display a formatted table, but to see how this looks as a CSV in plain text format, click the "Raw" format button.)

Hint: the “Free to Use Libraries” set contains sixty two (62) items, but you may not be able to easily retrieve each one.

### 2. Harvest the metadata for each item in the collection

Using the collection list, create a python function that will request the
full item metadata for each of the sixty-two items.
Save the JSON for each item locally, in a separate JSON file,
with a name corresponding to the item ID or LCCN.

### 3. Finishing the assignment

After completing this assignment, you should have your collection extraction python scripts,
collection lists, item metadata, and item digital files. Create all of this in a directory.
Your directory structure should look something like this:

```
collection-data-extraction
├── collection-extract-tools.ipynb
├── ftu-libraries-set-info.json
├── ftu-libraries-set-list.csv
├── item-files
│   ├── item-one-image.jpg
│   ├── . . . all of the images
│   └── item-sixty-two.jpg
└── item-metadata
    ├── item-one.json
    ├── . . . all the metadata
    └── item-sixty-two.json
```

#### Note

While the set has sixty two items, it may not be possible to harvest each item's metadata.
In that case, you can skip problematic items. But you should get the majority, at least fifty five or more items.[^1]

### Two Submission Options

**Option One:** a link to a file or folder in a GitHub repository where you have provided the files and saved the code.
It may be a private repo, as long as you have added the instructor as a collaborator with view permissions. The repo URL may be provided via Canvas.

**Option Two:** a zip file, uploaded on Canvas, that contains the extracted material in a directory.
These should all be in a directory containing python code in a `.py` or `.ipynb` file(s),
a list of the items in the collection in a JSON file,
the basic information for each item in the collection in a CSV file,
and a directory with JSON item files representing each item in the collection.

### Resources

* [Assignment submission on Canvas]({{ page.canvas-link }})
* [Sample Collection List CSV][sample-collection-list-csv]
* [Example pulling a collection list from loc.gov][loc-gov-collection-list-demo]
* [Example harvesting JSON item data and images from loc.gov][loc-gov-item-demo]

[loc-gov-collection-list-demo]: https://github.com/morskyjezek/si676-2025-data/blob/main/examples/assignment-extract-1-collection-list.ipynb
[sample-collection-list-csv]: https://github.com/morskyjezek/si676-2025-data/blob/main/collection-site-materials/collection_set_list-sample.csv
[loc-gov-item-demo]: https://github.com/morskyjezek/si676-2025-data/blob/main/examples/assignment-extract-2-collection-items.ipynb

### Notes

[^1]: There are 62 items in the "Free to Use Libraries" set, but it's likely that you will have a list of about 59 items in the end because not all of the items will produce a JSON file.
