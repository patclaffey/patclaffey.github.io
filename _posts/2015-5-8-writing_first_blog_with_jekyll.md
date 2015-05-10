---
layout: post
title: Getting Started with Jekyll to Blog on a GitHub Web-Site
---
Once I had my web-site configured on GitHub, and Jekyll installed and running on my desktop, I needed to learn how to write a blog using Jekyll.
So this is the subject of my second blog - my experience get started with Jekyll as a blog writing tool.

To get started as a Jekyll user I followed the advice given by Barry Clark in his article ["Build a Blog with Jekyll and GitHub Pages](http://www.smashingmagazine.com/2014/08/01/build-blog-jekyll-github-pages/).
This is a really excellent article and the perfect starting point for your journey as a Jekyll user.

##Getting Started using Barry Clark's Starter Jekyll Web-Site
I already had Jekyll installed and running on my desktop - but was missing the structure to launch a real web-site.
What Barry provides is a great seed or starter web-site that gets you up and running quickly with a real useful Jekyll powered web-site:

1. Barry has prepared a repository that follows Jekyll best practices.
This repository acts as the overall template for my web-site, and has saved me a ton of time.
Head to [Jekyll Now](http://www.github.com/barryclark/jekyll-now), and hit the “Fork” button in the top-right corner of the repository to fork a copy of the blog theme to your GitHub account.
Starting with a fork is great because it gives you a real Jekyll web-site to work with.
2. I went to my list of GitHub repositories and renamed Barry's forked repository to patclaffey.github.io - following GitHubs yourusername.github.io web-site naming convention.
I opened the internet url http://patclaffey.github.io in my browser and I now had a public Jekyll powered web-site.  That was really easy.  Thanks Barry!!
3. As a GitHub user I already have the git tool installed on my desktop.  I cloned the patclaffey.github.io repository to my desktop.
Now I had local desktop access to all the pages that comprise my new web-site.
4. I went to the root directory of patclaffey.github.io on my desktop.
I ran Jekyll from here, to build the local copy of my web-site by running the following command:
    bundle exec jekyll server   
I could now access the local desktop copy of my Jekyll web-site at the url [http://localhost:4000](http://localhost:4000)  on my desktop browser. 
5. I changed my website’s name, description, avatar and other options by editing the local copy of _config.yml file.
These custom variables were set up for convenience and are pulled into the theme when the website gets built.
Changing the local copy of _config.yml means I have to re-issue the "bundle exec jekyll server" to view the changes at [http://localhost:4000](http://localhost:4000).
Changes to any other file, except _config.yml, are visible at the local url without having to restart Jekyll.
To see these changes on my public web-site I just push the local changes using git to the GitHub repository.

##Creating my First Blog Post.

Now I just have to publish my first blog post:

1. All blogs are stored in the /_posts/ directory.
2. I edited /_posts/2014-3-3-Hello-World.md, deleting the placeholder content and entering my own.
3. I saved the file with a new file name.
Jekyll requires the text files that contain the posts to be named year-month-day-title.md.
I started the blog on the 6th of May.  So I saved the file with the name "2015-5-6-Getting\_Started\_Blogging\_on\_GitHub.md".
The files use the .md file extension where md stands for Markdown.
4. Now it is time to update the content of blog post in the the text file "2015-5-6-Getting\_Started\_Blogging\_on\_GitHub.md".
Those first few lines at the top of the blog post are called front matter. 
The front matter starts with line containing three dashes --- and ends with a second line containing three dashes.
Here is the front matter (first four lines) of my first blog:     
    ---    
     layout: post    
     title: Setting up a Web Site and Blogging Site on GitHub    
    ---     
Note that title is front matter does not have to match the title in the blog text file name,
The title in front matter appears on the web as the title of the blog post.


##Getting Started with Markdown.
The actual posts are written as text files and formatted using a convention called Markdown.
Markdown is very intuitive and quick to learn.
I use these [Markdown cheat sheets as a quick primer](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) on writing in Markdown.
The real power of Jekyll is its ability to generate web-sites from text files container Markdown.
The benefit of Markdown is that it lets you can focus on writing your content, greatly simplifying the formatting of the content.

{% comment %}
you have to set up a local development environment, install dependencies and figure out Jekyll’s build process.
{% endcomment %}









