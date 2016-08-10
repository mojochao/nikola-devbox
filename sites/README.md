# Adding Content

## Overview

Adding content and building sites is done with the **nikola** cli in
the *nikola-devbox* vm in this **repo/sites/** subdirectory or one of
the site subdirectories you create in it.

> $ vagrant ssh
> ubuntu@nikola-devbox:~$ cd repo/sites
> ubuntu@nikola-devbox:~/repo/sites$

For full instructions on how to use the **nikola** cli, check out
[The Nikola Handbook](https://getnikola.com/handbook.html).

## Create a site

Create a new site name with the **nikola new** command.  Replace
<SITENAME> above with your site name, and answer the prompts as you
like.  You can simply accept the defaults by pressing <return>.

Assuming we wished to create a site named *demo*.

> ubuntu@nikola-devbox:~/repo/sites$ nikola new demo

After this completes a subdirectory named for the demo site will have
been created.  Once a new site has been generated you should add it to
the git repo.

> ubuntu@nikola-devbox:~/repo/sites$ git add demo
> ubuntu@nikola-devbox:~/repo/sites$ git commit -m 'Initial drop of demo site'

You will need to be in a site directory to run the *build* and *serve*
commands.

> ubuntu@nikola-devbox:~/repo/sites$ cd demo
> ubuntu@nikola-devbox:~/repo/sites/demo$ 

## Build a site

Building a site transforms all your content into a static web site
that can be served by a web server.

> ubuntu@nikola-devbox:~/repo/sites/demo$ nikola build

## Preview a site

Once a site has been built, it can be served for preview.

Note that to preview the site you will need to use a web browser in
the host os.  The **nikola-devbox** vm does not have a graphical
desktop installed.

> ubuntu@nikola-devbox:~/repo/sites/demo$ nikola serve

Open the (generated site)[http://localhost:8000] in a web browser on
the host os to preview.

## Site Output

Once a site has been built, the generated static site is contained in
the *output* subdirectory.

> ubuntu@nikola-devbox:~/repo/sites/demo$ ls output
> archive.html     assets           categories       galleries        index.html       listings         robots.txt       rss.xml          sitemap.xml      sitemapindex.xml
> ubuntu@nikola-devbox:~/sites/demo$ 

These are the files that need to be uploaded to your production web
server's web root.
