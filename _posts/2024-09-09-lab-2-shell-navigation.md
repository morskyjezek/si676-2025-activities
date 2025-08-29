---
layout: post
title:  "Lab 2: File Navigation in the Shell"
date:   2024-09-09
due: 2024-09-15
categories: activities shell labs
canvas-link: https://umich.instructure.com/courses/698670/assignments/2472579
key: lab-2-key
published: false
---

![Sample file tree]({{ site.url }}{{ site.baseurl }}/assets/sample-file-tree.png)

Download the GitHub repo with sample files (as demonstrated in class), and then provide the shell commands that you would use to accomplish the following. Assume that command one begins when you are located in the directory called data. Note that the directory "data" should already exist in the repo files that you have downloaded from GitHub (it does contain some files and directories, but you will not need those for this exercise.)

1. Create the directory structure shown above, in the “data” folder (hint: to make this task less onerous, check out the man page for the `mkdir` command that allows you to make parents of a directory that don’t exist yet).
2. Create an `info.txt` file in the Michigan directory with the text "This is Michigan" and another in the Idaho directory with the text "This is Idaho".
3. Change your working directory to the Idaho directory.
4. Copy the `info.txt` file to the Montana and Louisiana directories.
5. Move the `info.txt` file in the Michigan directory to the `sample2` directory.
6. Add three lines of your choice to the `info.txt` file in the `sample2` directory.
7. Return to the `data` directory.
8. List the contents of your data directory in long form.
9. Display the contents of the `info.txt` file in the `sample2` directory
10. Delete the `info.txt` file in the sample2 directory
11. Delete the `Michigan` directory.

## Additional Activity

We worked through three fundamental Git processes in class. Review these and bring questions for discussion next week.

* Create a Git repo (`git init`), which you should only run in a new directory, or a directory that you want to connect to a GitHub project, which creates (or "initializes") a new Git repository
* Update a git repo (`add` --> `commit`), which moves changes into the staging area and then adds them into your Git log and repo record
* Push/pull a git repo (`push` and `pull`), which moves local changes to your remote repository (in our case on GitHub though it needn't always be)

For next week, aim to make sure you can create local repositories, connect them to a remote, and push changes to that remote.

## Resources

* [Accompanying slides][slides]
* [Assignment page on canvas]({{ page.canvas-link }})

[slides]: https://docs.google.com/presentation/d/1q-uz12RVq17JtYOtZ1wK7KwaACQhX4ai_tRYo1LYnBU/edit?usp=sharing
