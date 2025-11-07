---
layout: post
title:  "Lab: Working with MODS in XML"
date:   2025-10-30
assigned: 2025-10-31
due: 2025-11-06
categories: activities mods xml xpath python labs
canvas-link: https://umich.instructure.com/courses/779862/assignments/2877258
key: lab-8-key
published: true
---

For the following activities, answer using the [25 MODS records file (linked)](https://github.com/morskyjezek/si676-2025-data/blob/main/data/xml/2018_lcwa_MODS_25.xml). Use the [Jupyter notebook that explores MODS](https://github.com/morskyjezek/si676-2025-data/blob/main/examples/xml-working-with-MODS.ipynb) as a reference; many similar tasks are demonstrated there with the collection of 5 MODS records.

Work in a Jupyter notebook, as demonstrated in class, or a python file, to answer the following questions:

## Lab Questions

1. To make sure things are working, adapt the code from class that we used to count the individual MODS records in the file. How many are there?
2. These records contain `<subject>` elements, but only some of these correspond to headings that are authorized headings in the Library of Congress Subject Headings. Those are marked with the attribute `authority='lcsh'`, embedded in the element. Loop through `<subject>` tags, identify only the ones that include an LCSH attribute (use an XPath expression here), then print the content of those subject headings.
3. Data validation: Check the local call number references to ensure that they are in the proper format (e.g., `lcwaAddddddd` or `lcwaEddddddd`). Try adapting the [regular expression implementation illustrated in the sample MODS notebook under activities 6 & 7](https://github.com/morskyjezek/si676-2025-data/blob/main/examples/xml-working-with-MODS.ipynb). **Hint:** this is similar to what is demonstrated there, but you will need to modify the regex. Look carefully at the identifiers because some will be similar but won't match the expression we built in class. Question: how many correctly formatted identifiers for the LC web archives are there?
4. Data addition/modification (based on validation). This step builds on the previous validation question. Once you identify the local call numbers, then ensure they are properly formatted (validation), add a `type` attribute to indicate their source authority. Consult the [LC MODS documentation for `identifier` to see the usage instructions and valid attributes](https://www.loc.gov/standards/mods/userguide/identifier.html#type).
5. Save the updated records to a new file. To do this, assign the updated metadata element to an ElementTree, then use the write function to create XML (well-formed, has namespace declaration, and appropriate qualifiers for MODS and any other schemas used in the output).

When you are done, save your code file (as noted above, Jupyter notebook `.ipynb` or python `.py` is recommended) and answers outputs, then add to your course GitHub repository and provide the URL link to the assignment as your submission.

## Deliverables

- Upload your responses [via the Canvas assignment]({{ post.canvas-link }}).

## Resources

- [Intro to Basic XML Usage in Python (Jupyter notebook from course GitHub)][basics-notebook]
- [Building Basic, Well-Formed DublinCore records with Python XML tools][xml-basic-dublincore]
- [Slides from Class][xml-slides]

[basics-notebook]: https://github.com/morskyjezek/si676-2025-data/blob/main/examples/xml-intro-basic-functions-ET.ipynb
[xml-basic-dublincore]: https://github.com/morskyjezek/si676-2025-data/blob/main/examples/xml-generate-basic-dublin-core.ipynb
[xml-slides]: https://docs.google.com/presentation/d/15DZTqOlTvtdKlj1000XAhOVwUySbnoucMYHgQUyOncY/edit?usp=sharing
