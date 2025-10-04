---
layout: post
title:  "Lab: Installing & Configuring Omeka S"
date:   2025-10-02
assigned: 2025-10-03
due: 2025-10-09
categories: activities servers omeka labs
canvas-link: https://umich.instructure.com/courses/779862/assignments/2900388
key: #lab-6-key
published: true
---


This page contains the information for *{{ page.title }}*.

In this lab, you will be working to install and configure an instance of Omeka S on your servers. The process is a bit different than the process for the serverless sites, although the outcome (a published website that can host your digital content) is similar.

Your site will run on UMSI servers that are preconfigured with a LAMP stack. We are using some variation of the Platform as a Service model, where PaaS is provided by UMSI: they are providing the compute power, storage, database management, server connections, and domain registration to publish to the Web. You, meanwhile, are setting up the Omeka S software and making configurations to modify the backend and frontend of the software per the instructions.

In other words, UMSI is your cloud provider. In this case, they are running the LAMP stack (ie, Linux/Apache/MySQL/PHP), which provides the operating system, server, database, and program scripts that generate the HTML pages; Omeka provides all of the instructions to these systems to create the administration interface (backend) and the presentation for the public (frontend). We are able to interact with these systems using a shell interface (using basically the same commands and interactions that we used locally using the SSH or Secure Shell which provides security of data packets across the internet layer) and using the browser (we will be using an interface called cPanel, which opens up in the browser and provides access to the server).

To install and get Omeka S up and running, follow the instructions in [Omeka S Install Guide]({{ site.baseurl }}{% post_url 2025-09-25-omeka-s-install-guide %})

## Deliverables

- Upload your responses [via the Canvas assignment]({{ page.canvas-link }}).
