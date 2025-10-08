---
layout: post
title:  "Lab: Working with XML in Python"
date:   2025-10-08
assigned: 2025-10-10
due: 2025-10-16
categories: activities xml xpath python labs
canvas-link: https://umich.instructure.com/courses/779862/assignments/2877257
key: #lab-7-key
published: true
---

This is the page for *{{ page.title }}*.

## Lab Questions

1. What is the first-line string that declares an XML document (that is, what is basic syntax of the XML document declaration)?
2. What is the advantage of aliasing a library? In other words, why import the ElementTree module using `import xml.etree.ElementTree as ET` rather than the basic import statement?
3. Write a code block that loads the EAD finding aid in the course repo (`/data/xml/day_20221004_205435_UTC__ead.xml`). Parse the tree and extract the `archdesc` element. What are the subelements? This builds on the assignment we used in class (`control = root.find('ead:control')`) and then you can develop a loop, like `for element in archdesc` to explore further. (See the section in class exploring the `control` element.)
4. How do you work with prefixed namespaces in the ET module? How do you assign prefixes for use within path addresses? How do you assign namespaces for writing out a valid XML with namespace declarations and prefixes?
5. Write python code that will encode the following DublinCore fields in valid XML. The root tag should be `metadata`, it should output appropriately namespaced fields (i.e., using `dcterms:`). Encode the following fields:
```
title - Oldsmobiles Crossing the Mackinac Bridge
identifier - 2017-03-001.007.052
source - https://cadl.catalogaccess.com/archives/11662
provenance - https://www.cadl.org/
provenanceStatement - Original shared by the Capital Area District Libraries (CADL)
creator - Oldsmobile History Center
creator - https://cadl.catalogaccess.com/people/1320
created - Unknown
date - 1960s/1970s
subject - Lansing (Mich.)
subject - Ingham County (Mich.)
subject - Parades & processions
subject - Oldsmobile automobile
subject - Mackinac Bridge
subject - Bridges
subject - Cars
rights - Copyright Not Evaluated
rights - http://rightsstatements.org/vocab/CNE/1.0/
```

## Resources

* [XML Intro to Basic Functions notebook from course GitHub][worked-notebook]
* [Assignment page on Canvas]({{ page.canvas-link }})

[worked-notebook]: https://github.com/morskyjezek/si676-2025-data/blob/main/examples/xml-intro-basic-functions-ET.ipynb