---
layout: post
title:  "Adding Modules to Omeka S"
date:   2025-09-27
categories: guides omeka filezilla ssh
published: true
---


This guide describes the process of adding a Module to your Omeka S installation.
Note that Omeka also provides instructions on how to do this at [https://omeka.org/s/docs/user-manual/modules/#installing-modules](https://omeka.org/s/docs/user-manual/modules/#installing-modules),
but before you can follow those steps, you’ll need to add ("import") the module's files
to your server. That is, find the source code files, copy them, get them onto your server,
and put them where Omeka will look to find them.

This guide demonstrates the process of adding files to your server
with a combination of tools, namely `ssh` (a command line interface to your server’s OS)
and FileZilla (a graphical interface that provides secure access and aids the process of moving files between drives, in this case from your local drive to your server.

These instructions might also be called a "how to" demonstration
for using SSH and FileZilla. Note that [the process for logging in with Filezilla is illustated in the Filezilla login guide]({{ site.baseurl }}{% link _posts/2025-08-30-filezilla-guide.md %}).
The screenshots in the guide below show steps to install the [CSV Import module](https://omeka.org/s/modules/CSVImport/).

1. First, find the files you need in the Omeka S module registry: [https://omeka.org/s/modules/](https://omeka.org/s/modules/).
You will find many modules in the registry, and while you are welcome to install any that interest you,
there are a few critical modules that will support your digital collection term project, as described in the [Omeka S configuration guide]({{ site.baseurl }}{% link _posts/2025-09-26-omeka-s-configuration-guide.md %}).
2. Once you find the module you want, click the “Download” button. If there are multiple versions, it is usually best to choose the most recent unless there is some indication that that version is still under testing. The button should download a zip file to your computer.
![The CSVImport Module displayed in the Omeka S Module Registry]({{ site.url }}{{ site.baseurl }}/assets/omekas-csvimport-module-page.jpg "The CSVImport Module displayed in the Omeka S Module Registry"){:style="border: 1px solid black;"}
3. Now, use FileZilla to move the zip file from your computer to your server.
The zip file should be placed into the `modules` folder that you will find within the Omeka S folder that you have previously created on your server. (Follow [the usual process for working with Filezilla]({{ site.baseurl }}{% link _posts/2025-08-30-filezilla-guide.md %}).) To move the files, locate the downloaded zip file in left-hand panel window (showing files on your local computer), then click and drag it to the modules directory on your server in the right-hand panel window (showing files on your server).
![Transferring the downloaded zip file to the modules directory on the server with Filezilla]({{ site.url }}{{ site.baseurl }}/assets/omekas-transferring-module-filezilla.jpg "Transferring the downloaded zip file to the modules directory on the server with Filezilla"){:style="border: 1px solid black;"}
4. Now that the zip file is on the server, log in to your server via SSH in your terminal or command window.
To log in, use the same [process to log in to your server with SSH]({{ site.baseurl }}{% link _posts/2025-08-29-logging-in-to-your-server.md %}#ssh).
5. Finally, you can use the command line to unzip the files.
To do this, move your command prompt to the modules folder (while this command is context-dependent given the location of your window, your command will look something like `cd public_html/omeka-s/modules/`).When your prompt is located in the modules folder, check to confirm that the zip file is there (`ls -la`). Then, unzip command to open up the module (e.g., `unzip CSVImport-2.6.2.zip`).
![Unzipping the module with SSH in the modules directory]({{ site.url }}{{ site.baseurl }}/assets/omekas-unzipping-module-ssh.jpg "Unzipping the module with SSH in the modules directory"){:style="border: 1px solid black;"}

Once the files are moved into Omeka S's modules folder and unzipped,
you can follow the instructions in the [Omeka S guide for "Installing Modules"](https://omeka.org/s/docs/user-manual/modules/#installing-modules).

Additional modules can be added by following the same steps with any zipped package for an Omeka S module. For Assignment 2b, you need to install these modules:

- CSV Import
- Common
- OAI-PMH Repository
- Numeric Data Types

## Omeka-Related Resources

{% include omeka-guides %}
