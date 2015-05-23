---
layout: post
title: Configuring the GitHub Blogging Application
---
This blog is a work in progress.  Jekyll Now is the blogging application used for this site.
After installation
this application needs to be personalized for the individual web-site.
Application configuration is done by editing the configuration file, which is called _config.yml, using any text editor.

##Updating the "Jekyll Now" Configuration file
I changed my website’s name, description, avatar and other options by editing the local copy of _config.yml file.
These custom variables were set up for convenience and are pulled into the theme when the website gets built.
Changing the local copy of _config.yml means I have to re-issue the "bundle exec jekyll server" to view the changes at [http://localhost:4000](http://localhost:4000).
Changes to any other file, except _config.yml, are visible at the local url without having to restart Jekyll.
To see these changes on my public web-site I just push the local changes using git to the GitHub repository.



{% comment %}
you have to set up a local development environment, install dependencies and figure out Jekyll’s build process.
{% endcomment %}









