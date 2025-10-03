---
layout: post
title:  "Lab: HTTP Requests with Python"
date:   2025-09-24
assigned: 2025-09-25
due: 2025-10-02
categories: activities web http requests python labs
canvas-link: https://umich.instructure.com/courses/779862/assignments/2877256
key: lab-5-key
published: true
---


This page contains the information for *{{ page.title }}*.

**Note:** you may provide or share a link to a `.py` file or a Jupyter notebook (`.ipynb` is the file extension for notebooks) as your response.

## HTTP Requests with Python

### 1. URL / URI Formulation

Given the following lists of resources, form the URIs that will request the pages for each of the following items:

```
1. /resource/cph.3f05183/
2. /resource/fsa.8d24709/
3. /resource/highsm.64003/
```

**Hint:** As noted in class, you can locate these items by appending the resource identifiers to `https://www.loc.gov`.

### 2. LC Permalinks as URIs

The Library of Congress provides a standard "permalink" structure,
which is intended to be a stable identifier that can provide a consistent
URI for any item in the Library's collections.
The pattern for these URIs is `https://lccn.loc.gov/ + LCCN`.

Using the URIs that you created in the previous example, identify an LC permalink for each of the resources. To do this, look at the information provided about each resource, identify the LCCN, and then create the permalink.

### 3. Retrieve JSON data for items

The `loc.gov` website allows for responses to be requested in a data format, like JSON.
Using the same three items as above, write a block of Python code using the `requests` library that will request and retrieve the JSON data about the items above, then save them in local JSON files.

**Recall:** you can provide the parameter `fo` with the value of `json` to request the page "data" in JSON format.

### 4. Use a different parameter

Assume that the `https://www.loc.gov/search` address at the LOC can receive search requests by appending the parameter `q` to the URL.
This is a way to send a search query automatically via the URL (think of the variable `q` for "query").
Create a short block of Python code that queries the base URL.
Use the `input()` function so the code will ask the user for a unique query,
save that query as a string that will be inserted into the URI request as a parameter,
send the request using python requests,
and return the results.
The script should print out the results to the terminal or in the Jupyter notebook.
(In a production environment you would likely want to display such results in a browser or perhaps save them in a JSON file.)

## Deliverables

- Upload your responses [via the Canvas assignment]({{ page.canvas-link }}).
