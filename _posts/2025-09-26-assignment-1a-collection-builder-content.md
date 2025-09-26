---
layout: post
title:  "Assignment 1a: Adding Content to Your CollectionBuilder Site"
date:   2025-09-25
assigned: 2024-09-26
due: 2025-10-02
categories: assignments web collectionbuilder jekyll
canvas-link: https://umich.instructure.com/courses/779862/assignments/2877244
published: true
---


This page contains the information for *{{ page.title }}*.

**Note:** for the following questions that request Python code as your response,
you may provide or share a link to a `.py` file or a Jupyter notebook (`.ipynb` is the file extension for notebooks.)

## Part Two: Adding Content to Your CB Collection Site

This assignment builds on the CollectionBuilder template site that you created last week.
You should use the site you created in [last week's lab]({{ site.baseurl }}{% post_url 2025-09-18-lab-4-collectionbuilder %}).

Your task is to gather the components for the digital items represented by
the URIs located at the Library of Congress's namespace (i.e., `loc.gov`) and indicated in
the file (`loc-resource-list.txt`)[https://github.com/morskyjezek/si676-2025-data/blob/main/collection-site-materials/loc-resource-list.txt] located in the course data files repository.

You will need: a digital image file for each one, and as much metadata about each as you can find. Your goal is to restructure all of this into information
that CollectionBuilder can use, then republish it on your site.
Each item should publish on its own page and look something like [this sample page][sample-item-page].

### Decide on an identifier scheme

To link together the metadata and files comprising the digital objects,
you will need to create a standard naming scheme.
I suggest some combination of letters and numbers, joined together in a standard pattern.
For example, you could use some abbreviation of your collection, an underscore, and an item number, such as `nc_001` where `nc` is "new collection" with an appended iterated number after the underscore.
Another possibility would be to use the LCCN numbers for each object.

### Find and organize the digital objects

In some cases, the files may not be immediately downloadable.
In others, they will be easy to find.
In either case, you are looking for a high resolution digital image
in a jpeg or tif format. Once you locate the file, save it and rename it
according to the identifier scheme you created above.
Once the file is downloaded and renamed, move it to your site's `objects` directory.
Make sure the file's name matches the `objectid` column in your metadata spreadsheet.

### Record the metadata for each item

CollectionBuilder supports standard DublinCore elements for digital objects.
Consult each of the above resources, and complete the metadata entry for each one.
To do this, you may use the [sample CSV template provided in the course data repository][csv-template]

**Note**: to use the template, you can upload to GoogleSheets, edit there, then download a CSV copy to add to your collection site. Or, you can create in Python or another editor. Note that the CollectionBuilder docs suggest that editing the CSV in Excel will cause problems (due to the way that Excel encodes the CSV files, particularly line endings).

## Deliverables

* Link to your updated and working CollectionBuilder site,
  now populated with the five items you created metadata for
  (all still publishing from your GitHub repo)
* Invite the course instructor to collaborate on the repo

## Resources

* [Collection Builder Guide]({{ site.url }}{% post_url 2025-09-20-collectionbuilder-guide %})
* [Jekyll Guide]({{ site.url }}{% post_url 2025-09-02-jekyll-starter-guide %})
* [Assignment page on canvas]({{ page.canvas-link }})

[csv-template]: https://github.com/morskyjezek/si676-2025-data/blob/main/collection-site-materials/metadata-template-cb.csv
[sample-item-page]: https://morskyjezek.github.io/cb-test-turbo-octo-sniffle/items/nc_047.html
