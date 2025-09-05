---
layout: post
title:  "Setting Up a Jekyll Static Site"
date:   2025-09-02
categories: activities jekyll guides
published: true
---

This page contains tips and pointers on setting up your first Jekyll-based site
and publishing it with GitHub Pages.

## 1. Confirm you have the required dependencies

Jekyll runs on Ruby, and it requires Ruby, Ruby Gems, and a few other helper programs.
These are all described at the Jekyll documentation under "[Requirements](https://jekyllrb.com/docs/installation/#requirements)".

## 2. Before you use Jekyll, install it

This step installs Jekyll and also installs the "bundler," which helps create and serve the site later. If you have already done this, you don't need to do it again.

```
gem install jekyll bundler
```

## 3. Use the Jekyll Gem to Create Jekyll site in a New Folder

Now you can use Jekyll to create a new directory and set up all the basic elements for your Jekyll site. This will create the basic directory structure and many of the configuration files you need. In this example, you can install at a directory in your current terminal location called "test-site" (that is, `./test-site`).

```
jekyll new test-site
```

## 4. Move to that directory, look around, change, or serve your site

Move to the directory using `cd test-site`.

Once there, look for the basic folders, such as `_posts` or `_data`.
Depending on the Jekyll version and theme, you may not see all of the folders.
New pages can be created by copying from the `index.markdown` file
or by creating new markdown or HTML files.

**Tip: For any new pages, make sure you add page front matter gated by a three-hyphen line (`---`). You can copy this from existing pages or create your own. Common elements are `title`,
`permalink`, `date`, and `layout`, though every page will vary based on the content type and your site design.

To test your site and "serve" it locally, use the serve command from the terminal:

```
bundle exec jekyll serve
```

If things are working well, you should see something like this print on your terminal window:

```
      Generating... 
       Jekyll Feed: Generating feed for posts
                    done in 0.19 seconds.
 Auto-regeneration: enabled for '/Users/jajohnst/Desktop/si676-assignments-2024'
    Server address: http://127.0.0.1:4000//
  Server running... press ctrl-c to stop.
```

Copy and paste the server address (above, `https://127.0.0.1:4000/`) into a browser window, and you should see your site. To stop the server, press `Ctrl + C`.

## Some Challenges that You Might Encounter

* If you previously published a site in the repository using a file called `index.html`,
  you may find that nothing appears to change when you have started up and configured Jekyll.
  For example if you typed "Hello, World!" on the html page, and you still see plain
  text saying "Hello, World!" than you are likely in this situation.
  The 'old' index file is still publishing to your GitHub Pages site,
  and you should delete the old index file and push the changes to your remote repo.
  Hopefully you'll now see the updated Jekyll site.
* You will probably have `minima` as the default theme. You can change this if you'd like to experiment with the theming aspect of Jekyll. (For the purposes of SI 676, though, we won't work much with theming since Web design is beyond the scope of our course.) However, if you want to make changes in `minima`, or any other "gem based" theme (meaning the files are located in the Ruby package, and referenced when Jekyll builds the site, rather than the files being in your repo directory), [refer to this guide to find out where to find the theme files and how to import them for modification or customization](https://jekyllrb.com/docs/themes/#understanding-gem-based-themes).
* The GitHub Pages guide to Jekyll has useful information about publishing your site to your GitHub repo, and ultimately on how to publish it live to the web. Before you get to that point, however, it may be easier to work from the Jekyll documentation, which offers lightweight ["Quickstart" instructions that are more streamlined and useful for initiating, setting up, serving, and configuring your site locally and for testing prior to publishing](https://jekyllrb.com/docs/).

### Jekyll Resources

* How to Install Jekyll (locally), [https://jekyllrb.com/docs/installation/](https://jekyllrb.com/docs/installation/)
* Ruby 101 (as much as you need to know), [https://jekyllrb.com/docs/ruby-101/](https://jekyllrb.com/docs/ruby-101/)
* Serve and test your site locally [https://jekyllrb.com/docs/](https://jekyllrb.com/docs/)
* Information on using Jekyll with GitHub pages, [https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll)

### Related Lab

* See [Lab 3][related-lab]

[related-lab]: {{ site.url }}TODO link for jekyll lab
