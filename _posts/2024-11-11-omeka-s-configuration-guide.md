---
layout: post
title:  "Omeka S Configuration Guide"
date:   2024-11-11
categories: guides omeka
canvas-link: https://umich.instructure.com/courses/698670/assignments/2472573
published: false
---

This page describes how to configure Omeka S. Before taking these steps, you need to [install and set up Omeka S on your server]({{ site.baseurl }}{% link _posts/2024-11-10-omeka-s-install-guide.md %})

## Configuring Omeka S

These instructions also explain the main steps you must take to complete assignment #2 (see last step).  

These instructions assume that you already have a working Omeka S instance, and that you know how to sign in to your server. (Those steps were covered [in the install guide]({{ site.baseurl }}{% link _posts/2024-11-10-omeka-s-install-guide.md %}).)

1. Make sure that you write down and save somewhere your cPanel login credentials.
2. You will receive an email from the Omeka S installation. Save that, and also save your login credentials. Keep all of these items in a place where you can find them and where they are relatively safe.
  - For example, use the write it down in a notebook method
  - Or, pdf your emails and keep them in a folder on your computer.
3. Create a main user account beyond the Global administrator, which you will use for most of the activity that you undertake for the assignments. 
  - Keep a list of all the users, associated emails, and for those accounts you control, passwords.
  - I recommend a password manager (for all but the most sensitive login credentials), if you don’t already use one (Chrome and other web browsers typically have this built in; also, there are extensions you can install for most browsers that will help to generate random, secure passwords.)
4. Create a user for Jesse Johnston (supervisor level), using the email `jajohnst@umich.edu`.
5. Add in modules (we will go over the process in class, it involves FileZilla and SSH, and [is explained in the Omeka S Modules guide]({{ site.baseurl }}{% link _posts/2024-11-13-adding-omeka-s-modules.md %})). You must add:
  - [CSV Import module](https://omeka.org/s/modules/CSVImport/)
  - [Common](https://omeka.org/s/modules/Common/) - a helper module
  - [OAI-PMH Repository module](https://omeka.org/s/modules/OaiPmhRepository/)
6. Add at least one additional vocabulary. This process is described in more detail in the [Guide to Installing Vocabularies in Omeka S]({{ site.baseurl }}{% link _posts/2024-11-15-omeka-s-adding-vocabularies.md %}). For a quick start, use MODS ([Metadata Object Description Schema](https://www.loc.gov/standards/mods)). Use the “Vocabularies” option in the left menu, choose the “Import New Vocabulary”, then:
  - Name/Label: `MODS 1`
  - Namespace URI: `http://www.loc.gov/mods/rdf/v1`
  - Namespace prefix: `mods`
  - Vocabulary URL: `https://www.loc.gov/mods/modsrdf/v1/modsrdf.owl`
  - File format: `RDF/XML`
  - _Note: you may consider adding other vocabulary namespaces, but for this to happen smoothly with Omeka, any vocabulary you choose will need to be expressed in a standard linked data format specification (like RDF or OWL)._
7. Create at least one site (Omeka S allows you to administer multiple sites/collections)
  - Create an about page, with at least one image asset attached and a descriptive statement.

## Resources

* [Related slide deck illustrating the login process][related-slide-deck]
* [Guide to logging in to your server]({{ site.baseurl }}{% link _posts/2024-11-04-logging-in-to-your-server.md %})
* [Guide to Installing Omeka S on Your Server]({{ site.baseurl }}{% link _posts/2024-11-10-omeka-s-install-guide.md %})
* [Assignment 2b Submission on Canvas]({{ page.canvas-link }})

[related-slide-deck]: TBD