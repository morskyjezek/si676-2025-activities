---
layout: post
title:  "Lab: DNS and A Jekyll Static Site"
date:   2025-09-11
assigned: 2025-09-12
due: 2025-09-18
categories: activities web dns jekyll serverless labs
canvas-link: https://umich.instructure.com/courses/779862/assignments/2877253
key: #lab-3-key
published: true
---


This page contains the questions for the Lab on DNS and Jekyll

## GitHub Pages

_**NOTE:** There's not really anything to turn in for this section. Hopefully you worked through these first steps in class._

1. Set up a new GitHub repository and connect it to a repo on your local machine. It's likely you won't want to keep this around long term, so give it a name like `test-site-1` (or something similarly generic)
2. Activate GitHub pages for the repo you've created: [https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
3. Add a `README.md` (if you haven't already) and `index.html` so there is information in the repo, and also a published page; for this week, provide URL to repo and to published site
  * **HINT:** When you add an `index.html` file, put some text in it, like `Testing, Testing, 1, 2, 3, . . . ` otherwise you will get a blank page on your new site. 

## Jekyll

1. Initiate Jekyll in your local repo.
  * GitHub "[Create site with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)" - choose options for your operating system!
2. Publish your Jekyll serverless site to your GitHub repo (above site describes these steps as well).
3. Configure your Jekyll site:
  * Visit the `_config.yml` file, change the site name, description, and contact information.
  * Add at least one page (preferably modify the main home page or add another): [https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll#adding-a-new-page-to-your-site](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll#adding-a-new-page-to-your-site)
  * Add at least one "post" (more like a blog site): [https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll#adding-a-new-post-to-your-site](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll#adding-a-new-post-to-your-site)
4. Please add GitHub user @jesseajohnston to your repo as a collaborator. 
5. To complete the assignment, please provide the URL to the live Jekyll site with your changes.

### Jekyll Resources
  
  * How to Install Jekyll (locally), [https://jekyllrb.com/docs/installation/](https://jekyllrb.com/docs/installation/)
  * Ruby 101 (as much as you need to know), [https://jekyllrb.com/docs/ruby-101/](https://jekyllrb.com/docs/ruby-101/)
  * Serve and test your site locally [https://jekyllrb.com/docs/](https://jekyllrb.com/docs/)
  * Information on using Jekyll with GitHub pages, [https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll)

## DNS Questions

1. Use the `dig` command to query `umich.edu`. What is the response and how would you explain it?
2. Use the command for the above response, and pipe the output to a file named `umich-dns-record.txt`. Provide the text file.
3. Use the `dig` command to query `umich.edu`. What is the command to return only the "answer" section of the response?  

## Bonus

4. Note that you can ask for multiple domain names. For example: `dig +noall +answer si.umich.edu umich.edu wisc.edu education.wisc.edu`. The response is a good use case for a tool like `awk`. If you use a pipe to route the data from dig to awk, can you produce a comma-separated-values-like output of just the domain and the IP address? 
  * The `awk` command is actually a sort of mini program language, particularly useful for querying and parsing text files with columns. If you want to learn more about it, you can look at the G-AWK manual at [https://www.gnu.org/software/gawk/manual/gawk.html](https://www.gnu.org/software/gawk/manual/gawk.html). It is very useful for parsing data in columns, which is a frequent pattern seen in the command line/text interface. Variables are named with dollar signs `$1` and the output patterns are enclosed in curly braces `{}`. This should be very similar to the exmaple presented in the slack channel, but you will need to add in a comma for the output.

## Resources

* [Accompanying slides][slides]
* [Assignment page on canvas]({{ page.canvas-link }})

[slides]: https://docs.google.com/presentation/d/1E8HexG1lsBXvF8NCetEsjxatbbMdWikADyXlVNT83GE/edit?usp=drive_link
