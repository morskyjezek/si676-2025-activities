---
layout: post
title:  "Omeka S Guide: Fix Thumbnailer"
date:   2024-12-01
categories: guides omeka
published: false
---

This guide describes how to modify some of the Omeka S files so that your site can autmatically create thumbnail images. Omeka S uses an external, open-source library called [ImageMagick](https://en.wikipedia.org/wiki/ImageMagick) for standard image manipulations like resizing, cropping, creating thumbnails, etc. Without the fix described below, ImageMagick fails when Omeka calls it because it uses a command that is not available in the our servers' operating system.

In brief, this fix makes small modifications to one PHP file in Omeka, which removes the conflict with ImageMagick. This course does not require PHP, but essentially by implementing this fix you are doing a small bit of work in PHP. This quick fix is something that will work for the purposes of your Omeka sites, but it is not something that I would recommend as a long-term solution, nor something that you would want to implement in a production environment without further testing and consultation with the IT department.

The steps outlined here use terminal (command line/bash shell), SSH, and the nano text editor. You could make these changes with other tools, but since we've been practicing these skills throughout the term, this is good practice.
A screencast demonstrating the process is embedded at the end of this guide.

## Step-by-step Instructions

Follow these steps to modify the way that Omeka S calls ImageMagick so that it will generate thumbnails:

1. Log in to your server using a command shell (that is, terminal, GitBash, etc)
2. Locate the file that you need to modify:
  - You need to modify a file called `ImageMagic.php`. This file is located in Omeka S's core files, which were installed when you set up your Omeka S instance. The file is located in a folder called `application`, which contains most of these core files. If your Omeka S home directory was called `omeka-s`, then the relative path is as follows: `omeka-s/application/src/File/Thumbnailer/ImageMagick.php`.
  - Finding the file:
    - First, navigate to the folder where Omeka S is installed. In my server, that is `public_html/omeka-s/` (this is the folder where the files were initially installed if you installed to a directory named `omeka-s`).
    - In your main Omeka folder, you should see the "application" folder, which is where most of the Omeka core files are located. You’re looking for this path: `application/src/File/Thumbnailer/`. Navigate to that path using the `cd` command.
  - To navigate to this folder from your first login (when you are at the “root” of your server), the command for an Omeka S installation in a directory named `omeka-s` will look something like this:
  ```bash
  $ cd public_html/omeka-s/application/src/File/Thumbnailer/
  ```
3. This step assumes you have navigated your prompt to the `Thumbnailer` folder (as described above in Step 2). Now, open `ImageMagick.php` using a text editor. Suggestion: use the **nano** editor. You can open the file with nano using a command like this: `nano -l ImageMagick.php`. This command opens nano, the `-l` option requests nano to open with a display that shows the line numbers, and then the command designates the file that you want to open. The window should look something like this (the first line of the display should show the name of the file you are editing):
![The ImageMagick.php file opened in nano]({{ site.url }}{{ site.baseurl }}/assets/omeka-imagemagick-in-nano-php.jpg "The ImageMagick.php file opened in nano"){:style="border: 1px solid black;"}
4. Now, make these edits in the file:
  - On line 59: add two forward slashes (`//`) to the beginning of the line.
  - On line 70: add two forward slashes (`//`) to the beginning of the line.
    - _Pro Tip:_ Use the keyboard command `CTRL + _` to select the line you want to go to directly (it is much quicker to move around in text files like this, if you know where you're going).
    - **Explanation:** Two slashes (`//`) indicate a comment in PHP (like the `#` character in Python). By making these changes, you are effectively modifying the PHP code to skip over these lines. The reason for this is that the command that is being called on this line (an argument `-active` is being sent to ImageMagick but it does not work in our version of ImageMagick).
    After editing line 59, the nano display should look something like this:
    ![The ImageMagick.php file edited on line 59]({{ site.url }}{{ site.baseurl }}/assets/omeka-imagemagick-edited-nano-php.jpg "The ImageMagick.php file edited on line 59"){:style="border: 1px solid black;"}
5. Finally, save the edited file. In nano:
  - Type `CTRL + O` to "write out" (that is, save) the file
  - When you are asked to confirm the name (“File Name to Write:”), press Enter. the name should be the same as the original file.
  - Type `CTRL + X` to exit ("eXit") nano
  - Nano will close and you should again see the command prompt in the shell.
6. If these edits were entered correctly and the file was saved, your thumbnail generator should now work when you use the Import CSV module to add in items.

## Step-by-step Video

<iframe width="560" height="315" src="https://www.youtube.com/embed/VwCh7L8L2hc?si=2Fw8OamoOCB_gRxO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

{TODO: add video embed [https://youtu.be/VwCh7L8L2hc](https://youtu.be/VwCh7L8L2hc) and also embedded at}