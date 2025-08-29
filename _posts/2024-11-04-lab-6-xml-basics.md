---
layout: post
title:  "Lab 6: Working with XML in Python"
date:   2024-11-04
assigned: 2024-11-04
due: 2024-11-10
categories: activities xml xpath labs
canvas-link: https://umich.instructure.com/courses/698670/assignments/2472584
key: lab-6-key
published: false
---

This page contains the information for *{{ page.title }}*.

## Lab Questions

1. What is the first-line string that declares an XML document (that is, what is basic syntax of the XML document declaration)?
2. What is the advantage of aliasing a library? Why import the ElementTree module using `import xml.etree.ElementTree as ET` rather than the basic import statement?
3. Write a code block that loads the EAD finding aid in the course repo (`/data/xml/day_20221004_205435_UTC__ead.xml`). Parse the tree and extract the `archdesc` element. What are the subelements? This builds on the assignment we used in class (`control = root.find('ead:control')`) and then you can develop a loop, like `for element in archdesc` to explore further. (See the section in class exploring the `control` element.)
4. How do you work with prefixed namespaces in the ET module? How do you assign prefixes for use within path addresses? How do you assign namespaces for writing out a valid XML with namespace declarations and prefixes?

## Resources

* [XML Intro to Basic Functions notebook from course GitHub][worked-notebook]
* [Assignment page on Canvas]({{ page.canvas-link }})

[worked-notebook]: https://github.com/morskyjezek/si676-2024-data/blob/main/examples/xml-intro-basic-functions-ET.ipynb
