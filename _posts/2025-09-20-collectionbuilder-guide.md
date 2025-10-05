---
layout: post
title:  "Collection Builder Starter Guide"
date:   2025-09-20
categories: guides jekyll collectionbuilder serverless
published: true
---

This page contains tips and pointers for working with CollectionBuilder.
CollectionBuilder provides code that generates a static site using the
Jekyll static site platform.

## Item Metadata

The CollectionBuilder documentation has two useful templates that you can
use to format metadata for the objects in your collection. While these are
very useful for demonstration purposes, it is also helpful to have an
idea about what these various fields are, where they are displayed on the site,
and some general conventions or usage guidelines.
This section offers some more detailed information about these aspects of CollectionBuilder metadata.

![CollectionBuilder item page]({{ site.url }}{{ site.baseurl }}/assets/cb-item-page.jpg)

Note above that the metadata elements for the still image shown largely match
DublinCore fields. This shows that most digital objects in CollectionBuilder can be displayed and managed with standard descriptive metadata elements based on DublinCore.
Even so, there are a few specialized fields that aid CollectionBuilder in managing the digital objects. If you upload your metadata in a CSV file, then the following can be used as a guide to fields that you can use:

| CSV header | Required? | DublinCore field? | Explanation |
| ------     | ------    | ------            | ------ |
| objectid   | Y         | N                 | Must match the name of any associated digital files |
| title      | N         | Y                 | A title for the resource |
| creator    | N         | Y                 | An entity responsible for making the resource |
| date       | N         | Y                 | A date assocationed with the resource |
| description | N        | Y                 | An account of the resource |
| subject     | N        | Y                 | 	A topic of the resource |
| location | N | Y | A spatial region or named place. Extended DC element [location](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/terms/Location/). |
| latitude | N | N | Can be provided if you want the item to appear on the mapping page |
| longitude | N | N | Can be provided if you want the item to appear on the mapping page |
| source | N | Y | A related resource from which the described resource is derived. Extended DC element [source](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/terms/source/) |
| identifier | N | Y | An unambiguous reference to the resource within a given context. Typically something like an ISBN, DOI, URN, or local unique identifier. DublinCore term [identifier](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/terms/identifier/) |
| type       | N | Y | The nature or genre of the resource |
| format     | N | Y | The file format, physical medium, or dimensions of the resource |
| language   | N | Y | A language of the resource |
| rights     | N | Y | Information about rights held in and over the resource |
| rightsstatement | N | N | Use to provide a non-literal value that explains the rights statement. Typicaly URIs may be for Creative Commons License or rightsstatements.org |
| display_template | N | N | A CollectionBuilder specific field that can direct how an object is displayed; useful for specialized media types like pdfs, audio, or video items |
| object_location | Y | N | This field should provide a path to the associated digital file(s), must be provided if a surrogate is to appear |
| image_small | N | N | Path to a small or mezzanine copy of the digital object; must be provided for a surrogate to appear on Browse page |
| image_thumb | N | N | Path to a small copy suitable for thumbnail image; must be provided for a surrogate to appear in searches, on featured pages, or browse pages |
| image_alt_text | N | N | Should be provided for accessibility purposes; provides a text description of the associated image |
| object_transcript | N | N | Should be provided for items that have transcribed text, such as oral histories, or handwritten items |

For the most part, individual elements are optional. Notice that as more information is provided, the item page will expand to fit those elements. If you require additional elements for items, then it will be necessary to modify the item page display layouts and other modifications.

## Creating Digital Objects

CollectionBuilder requires pre-loaded access copies of various resolutions.
Although this could be managed by hand, the framework includes a small version and thumbnail copy generator. Information about this can be found on the [Creating Digital Derivatives](https://collectionbuilder.github.io/cb-docs/docs/walkthroughs/derivatives-walkthrough/) walkthrough.

## Useful Links

While this page will provide some insight on frequently asked questions,
you should use the excellent documentation from the CollectionBuilder
project. If you have been able to
a) create and publish your own Jekyll site from GitHub, and
b) pull metadata from the Library of Congress API,
then their documentation should be sufficient to get your own
Collection Builder site going:

* CollectionBuilder: [CSV Walkthrough](https://collectionbuilder.github.io/cb-docs/docs/walkthroughs/csv-walkthrough/)
* CollectionBuilder: [Creating Digital Derivatives](https://collectionbuilder.github.io/cb-docs/docs/walkthroughs/derivatives-walkthrough/) from original digital files
* CollectionBuilder: [Working with GitHub](https://collectionbuilder.github.io/cb-docs/docs/walkthroughs/gh-walkthrough/)
