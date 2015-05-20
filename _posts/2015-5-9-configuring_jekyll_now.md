---
layout: post
title: Configuring Jekyll Now Blogging Application
---
This blog is a work in progress.  The topic for this post is using the Jekyll Now configuration file to personalize the blogging web-site.



##Updating the "Jekyll Now" Configuration file
1. I changed my website’s name, description, avatar and other options by editing the local copy of _config.yml file.
These custom variables were set up for convenience and are pulled into the theme when the website gets built.
Changing the local copy of _config.yml means I have to re-issue the "bundle exec jekyll server" to view the changes at [http://localhost:4000](http://localhost:4000).
Changes to any other file, except _config.yml, are visible at the local url without having to restart Jekyll.
To see these changes on my public web-site I just push the local changes using git to the GitHub repository.



{% comment %}
you have to set up a local development environment, install dependencies and figure out Jekyll’s build process.
{% endcomment %}









