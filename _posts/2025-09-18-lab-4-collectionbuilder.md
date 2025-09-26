---
layout: post
title:  "Lab: Setting Up CollectionBuilder"
date:   2025-09-18
assigned: 2025-09-19
due: 2025-09-25
categories: activities web jekyll collectionbuilder labs
canvas-link: https://umich.instructure.com/courses/779862/assignments/2877254
key: lab-4-key
published: true
---

This page contains the information for *{{ page.title }}*.

This assignment is similar to last week's: you are setting up a Jekyll site, but this time
you will usie an existing site structure and framework called CollectionBuilder (CB).
First, you will need to set up a new repo (I would suggest something `collection-builder-test` or `demo-collection`).
Then, make sure it works with Jekyll.
Finally, install and configure the CollectionBuilder platform.
To do this, follow the instructions at CollectionBuilder: [CSV Walkthrough](https://collectionbuilder.github.io/cb-docs/docs/walkthroughs/csv-walkthrough/).

Once set up, make some basic modifications to your site (most of these can be changed in the `_config.yml` file):

- Give your site an original name
- Selecting an alternative featured image (what appears on the main page behind the site title)
- Modify the text on the "About" page (note that in the CB Builder framework, all of the top-level pages are in a folder called `pages`) and you should see some markup text there already as a placeholder (remove that text and add in something of your own)

**Note 1:** Keep your thinking hats on. There are a few steps in the CB guide that you won't need to follow exactly (for example, you don't need to sign up for a GitHub account, you already have that). Your goal is a working site, the instructions give you the steps to get there, but there may still be some specific issues you will need to address for your site.

**Note 2:** If you see any errors about missing packages or helpers, note that you should not need ImageMagick or GhostScript at this point, unless you want to experiment with adding objects and metadata of your own.

## Deliverables

- Link to a published, and working CollectionBuilder site, using the sample content from CB, publishing from a GitHub owned by your account, and the corresponding GH repository.
- Invite the course instructor to collaborate on the repo

## Resources

- [Jekyll Guide]({{ site.url }}{% link _posts/2025-09-02-jekyll-starter-guide.md %})
- [Assignment page on canvas]({{ page.canvas-link }})
