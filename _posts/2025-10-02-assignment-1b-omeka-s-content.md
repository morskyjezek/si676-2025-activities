---
layout: post
title:  "Assignment 1b: Adding a Site & Content to Your Omeka S Installation"
date:   2025-10-01
assigned: 2024-10-03
due: 2025-10-16
categories: assignments web omeka servers
canvas-link: https://umich.instructure.com/courses/779862/assignments/2877245
published: true
---

In this assignment, you will be working to add sample collection content to your a new Omeka S that runs in the [previously installed Omeka S platform]({{ site.baseurl }}{% post_url 2025-10-02-lab-installing-omeka-s %}).

## Configuring Your Omeka S Installation

This assignment builds on the Omeka S site that you previously created.
Your site and content should be created in the Omeka S installation from [last week's lab]({{ site.baseurl }}{% post_url 2025-10-02-lab-installing-omeka-s %}).
To the basic installation you already have, you will complete the site configuration, including:

1. Add Omeka S Modules
2. Add Vocabularies
3. Add an Omeka site

### 1. Add (Install) Omeka S Modules

In this step, you are adding new Omeka S modules, which will extend Omeka's functionality.
To add modules, follow the steps in the [Adding Modules to Omeka S guide]({{ site.baseurl }}{% post_url 2025-09-26-omeka-s-adding-modules %}).

### 2. Add (Install) Vocabularies

In this step, you are adding a controlled vocabulary to Omeka S. The general idea is similar to adding a module, as it does add functionality, but this step can be completed within Omeka, it does not involve adding new files to your server. To add a vocabulary, follow the steps in the [Adding Vocabularies to Omeka S guide]({{ site.baseurl }}{% post_url 2025-09-26-omeka-s-adding-vocabularies %}).

### 3. Add (Create) a New Site in Omeka S for a Sample Collection

The [sample CSV template for Omeka][csv-template] demonstrates how to structure the import CSV.

### Load Sample Collection Content

Use the same collection items that you added to your CollectionBuilder site in Assignment 1a.
To do this, you can reuse the digital objects that you already gathered from the Library of Congress.
That is, the same items from Assignment 1a, as indicated in the file [`loc-resource-list.txt` located in the course data files repository](https://github.com/morskyjezek/si676-2025-data/blob/main/collection-site-materials/loc-resource-list.txt).

Your task is to restructure all of this into a format that allows you
to load it into Omeka S, then republish it on the new Omeka site you created.
Each item should publish on its own page and look something like [this sample page][sample-item-page].

## Written Reflection

The final component of the Assignment 1 is to write a short reflection (300-500 words) about the process of collecting the collection items, and the difference between working with a serverless site (in this case, CollectionBuilder) and the sites on the server you're maintaining (in this case, your Omeka S installation). While you do not have to answer each question, please use the following questions to guide your reflection:

- What perspective on open source software does this give you? Have you changed any of your thoughts about the pros and cons of open source software?
- What steps were the easiest or most difficult? What was most confusing, or most clear?
- Given the work involved, how satisfied are your sites as they stand so far?
- If you have previously used Omeka (as a Software as a Service model), how do you feel about it now that you have had to set everything up (more like a Platform as a Service)?

## Deliverables

- Your Omeka S platform now includes the specified modules and vocabularies
- Link to your new Omeka S site, populated with the four items and their metadata
- Invite the course instructor as a user in your Omeka S site
- Short written reflection (300-500 words)

## Resources

- [Installing Omeka S Guide]({{ site.url }}{{ site.baseurl }}{% post_url 2025-09-25-omeka-s-install-guide %})
- [Assignment page on canvas]({{ page.canvas-link }})

[csv-template]: https://github.com/morskyjezek/si676-2025-data/blob/main/collection-site-materials/metadata-template-omekas.csv
[sample-item-page]: TBA
