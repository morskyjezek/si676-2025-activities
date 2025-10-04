---
layout: post
title:  "Omeka S Install Guide"
date:   2025-09-25
categories: guides omeka servers
published: true
---

This page describes how to install Omeka S on your servers. This is a multi-step process, which requires you to gather the Omeka S files, configure and prepare them, set up a database for the platform to use, and finally making all of that work on your LAMP server.

In case you were wondering, it is unlikely you would have to install the tools in this way, but hopefully this will help you to see how the various components fit together. It is more likely that your server will have a tool that helps you to install things like this. One common one is called *Softaculous*. Installing Omeka "manually" like this requires you to work with the various elements of the overall LAMP server architecture, particularly the file system - LINUX - and databases - MySQL. The Apache server is handling the HTTP requests and tasks that display the cPanel interface, and any of the interactions between the platform components are likely communicating to the databases via PHP.
For the most part, though, you don’t need to worry about how those components interact once this installation step is completed.

## Installing Omeka S Manually

The manual install process has a few main steps:

1. Configure your server (i.e., "get the server ready"):
  - Ensure there's a place where Omeka S can "live" on the server.
  - Set up a database and database user agents.
2. Configure the Omeka S files (i.e., "get the files for the application ready"):
  - Download the Omeka S files (in .ZIP) from the Omeka server at <https://omeka.org/s/download/>.
  - Unzip the files locally and prep them (this is mostly the addition of your database user information).
3. Put the files on the server. This is mostly transferring the Omeka S program files to your server.
4. Configure the web application (i.e., "set up Omeka S"). This is relatively basic and involves creating an initial login for the Omeka S installation you have created.

The process explained in detail below is also [outlined in the Omeka S User Manual](https://omeka.org/s/docs/user-manual/install/), but the details of the steps are not described. Here are those steps described as they should be carried out on your LAMP server:

### Configure Your Server

Main steps include:

* Create a directory for the Omeka files in your server’s folder called: `public_html`
* Create a new database in the SQL server
* Create a new database user and password
* Assign that user to the new database

#### Create a Directory for Omeka S on Your Server

Check your server's `public_html` directory to ensure there are no files where you want to put your Omeka S install. There are various ways that you can do this. You can use the file manager tool within cPanel, you can use `ssh` and the shell, or you can view the directory using FileZilla. **Whatever option you choose, make sure that there is no existing folder with the name you plan to use in your `public_html` directory.** Keep in mind that the folder name of your Omeka S files will form the URLs for your repository, so choose something descriptive but also simple, like `omeka` or `omekas`.

In the above example, if your username was `umsifan` and you place your Omeka S files in `omekafan`, your site’s URI would look like this:

```
http://umsifan.si676.si.umich.edu/omekafan/
```

#### Create a New SQL Database on Your Server

There are various ways to do this, but for ease of use (and also because this is not a class about SQL), I suggest using the interactive Databases tool within cPanel.

To do this, click on “MySQL Databases” under “Databases” in cPanel. In the databases tool, you will complete the form for “Create New Database,” which is where you should type the name of the database that you want, then click on “Create Database.” The name you choose will be appended to your username after an underscore, and in a sense is like a namespace, providing a unique alias for your database even though there are likely thousands of database tables out there named omeka. It will look something like this, if you wanted to create a new database named `jajohnst_new_omeka_db`:

![Creating a new database for your Omeka S install]({{ site.url }}{{ site.baseurl }}/assets/omeka-newdbs.jpg "Creating a new database for your Omeka S install"){:style="border: 1px solid black;"}

#### Create a database User Agent (username and password)

Scrolling down in the databases tool, create a username and password combination. You won’t need to use this frequently, but you will need to enter the pair in your .ini file, so make note of the username and password that you create. You are essentially creating credentials for a local “user agent,” which will interact with the databases on behalf of Omeka S. If you want to randomly generate a password, use the “Password Generator” button or try an online tool like [https://www.avast.com/en-us/random-password-generator#mac](https://www.avast.com/en-us/random-password-generator#mac). Remember when you create the password, write it down or copy it to a safe place before proceeding. You will need to reuse it later.

![Creating a new user agent for your database]({{ site.url }}{{ site.baseurl }}/assets/omekas-db_user.jpg "Creating a new user agent for your database"){:style="border: 1px solid black;"}

#### Assign the user to the database

Finally, assign the user to the database. This makes use of the “Add User to Database” section of the database tools. Here, select the user you created, then select the database, and click “Add.” In the screen that follows, select all of the permissions (you want this user to be able to do all the things with the databases that Omeka S will need!):

![Adding user to the database]({{ site.url }}{{ site.baseurl }}/assets/omekas-assignuserdb.jpg "Adding user to the database"){:style="border: 1px solid black;"}

### Configure the Omeka S files

Now, it's time to get the files for Omeka S.

#### Download Omeka S

Download the entire package of files for Omeka S from the Omeka website at: [https://omeka.org/s/download/](https://omeka.org/s/download/). This should arrive in a zip format. Unzip the files and take a look. It is interesting to look around the files and get an idea of how they are structured.

Notice, for example, there are a lot of `.php` files but not many `.html` files. Why do you think that is?

#### Prepare Omeka S files locally

After you’ve looked around, **find the file `database.ini` in the folder named `config`**. This file contains the information that allows the Omeka files to talk to the SQL database. It has to have a user, a password, a database name, and a host name. This information will be used by the PHP files in Omeka to write new information to the database, create, read, update, delete, or whatever else it may need to do to access information in the database.

You can open this file as a plain text file using VSCode, or any other text editor. When you open the file, it should look like this:

![Configure the database connection]({{ site.url }}{{ site.baseurl }}/assets/omekas-assignuserdb.jpg "Configure the database connection"){:style="border: 1px solid black;"}

Enter the information from the database that you previously created on the server. This will vary based on the names that you chose, the host name should always be “localhost”. Thus, the information should look something like this, if your user was `omekas_db123`:

```
user     = "omekas_db123"
password = "secret123"
dbname   = "omekas_db123"
host     = "localhost"
```

Once you have the information entered, **make sure you save the file**.

Finally, create a zip file of the folder containing all of the Omeka S files, and name it what you want your endpoint URL to be. For example, if `umsifan` wants their site to be at `https://umsifan.si676.si.umich.edu/omekafan/`, they should name their zip file
`omekafan.zip`.

### Put the Omeka S files on the server

Once your zip file is saved, use FileZilla to transfer the files to the server in the `public_html` folder.

After the file transfer process is complete, you should be able to navigate in the browser to your server’s URL, and then add the name of the Omeka S directory at the end to display the Omeka S interface. It will look something like this:

![Install Omeka S - first user]({{ site.url }}{{ site.baseurl }}/assets/omekas-firstuser.jpg "Install Omeka S - first user"){:style="border: 1px solid black;"}

### Omeka S is Ready to Go

If you are seeing a page like the one above, then your Omeka S instance should be ready to go. To get started, fill in the initial user form and click the “Submit” button at the bottom of the page.

There is more work to do to get sites and collections running, but if you completed the above, then your Omeka S platform is ready to go. The next steps will be to configure Omeka S so it can publish new sites, modules, users, and the collection content. These will be parts of the next assignment and described in the [Omeka S configuration guide]({{ site.baseurl }}{% link _posts/2025-09-26-omeka-s-configuration-guide.md %}).

## Resources

* [Related slide deck illustrating the Omeka S install process][related-slide-deck]
* [Guide to logging in to your server]({{ site.baseurl }}{% link _posts/2025-08-29-logging-in-to-your-server.md %})

[related-slide-deck]: https://docs.google.com/presentation/d/1krzUOhkDnHrA0Z_SOdWqmS70SbLF0pD4_7p4VQkvnkQ/edit?usp=sharing
