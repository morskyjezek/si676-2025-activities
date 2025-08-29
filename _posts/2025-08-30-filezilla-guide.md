---
layout: post
title:  "Using FileZilla"
date:   2025-08-30
categories: guides filezilla
published: false
---

This page describes using FileZilla.
There is a large amount of overlap between this guide and the [guide to logging in to your server]({{ site.baseurl }}{% link _posts/2025-08-29-logging-in-to-your-server.md %}).
FileZilla is a graphical interface software that you can use to
view, manage, and transfer files between your computer and the server using the SFTP protocol
(that is, Secure File Transfer Protocol).

## FileZilla for File Management (FTP/SFTP) {#filezilla}

The Filezilla client provides a graphical user interface allowing you to use
secure File Transfer Protocol (SFTP and FTP) tools.
The Filezilla software is available at Campus Computing sites and is also available
for a 30-day trial version if you wish to download it on your own computer
(see the [Filezilla site for download information](https://filezilla-project.org/download.php)).

![Filezilla client window]({{ site.url }}{{ site.baseurl }}/assets/filezilla-main-window-macos.jpg "Screenshot of the Filezilla client with main areas highlighted"){:style="border: 1px solid black;"}

In the above screenshot, take note of the three main parts of the window.
In the area of rectangle 1., you can see the current status of the connection, any file transfers that you execute, and sometimes useful updates as to what Filezilla is doing.
In the area of rectangle 2., you have a file browser window that shows files on your local computer (in the above screenshot, it is showing the `jajohnst` directory in my laptops `Users` folder at the root of the operating system indicated by the leading slash `/` of path you see in the "Local site:" bar above the rectangle).
In the area of rectangle 3., you see a similar file browser. This file browser, however, shows the files on your server. (Note that it will only show those files when you are logged in.)

When you are logged in, you can use FileZilla to move files from your local computer to the server, or from the server to your local computer, by clicking and dragging and dropping. similarly to how you would do so in a graphical file browser window (like "Explorer" or "Finder"). Note that you may on some occasions be asked to confirm or renew your login (the password or dual factor process may repeat).

For a description of how to log in to your server with FileZilla, see the [Guide to logging in to your server, FileZilla section]({{ site.baseurl }}{% link _posts/2025-08-29-logging-in-to-your-server.md %}#filezilla).
