---
layout: post
title: Installing Blogging Software for GitHub
---
A GitHub web-site is like an empty container.
A blogging application is needed to transform this empty container into a functional blogging web-site.
A blogging application is software that manages the layout, formatting and style of the users blogs on the blogging web-site.
In the case of GitHub this blogging software needs to be compatible with Jekyll.
This blogs describes installing up this essential blogging software.


The blogging software installed in this web-site is called "Jekyll Now" and is written by Barry Clark.
Think of "Jekyll Now" as WordPress for GitHub.
Barry has written a fantastic magazine article ["Build a Blog with Jekyll and GitHub Pages](http://www.smashingmagazine.com/2014/08/01/build-blog-jekyll-github-pages/)
on how to install his blogging software.
This is an excellent article and required reading for setting up a blogging site on GitHub.

##Installing "Jekyll Now" Blogging Application in my GitHub Account
Jekyll Now is like WordPress for GitHub- its the essential blogging software for GitHub.
The "Jekyll Now" blogging software is stored in Barry Clark's public GitHub account.
You need a copy of this software.
As a GitHub user it is really easy to copy software between GitHub accounts - it's called making a fork of a repository.

1. To fork Barry's blogging application click on the link [Jekyll Now](http://www.github.com/barryclark/jekyll-now), and hit the “Fork” button in the top-right corner of the repository.
2. My GitHub account now has a new Jekyll Now repository.  This is my own personal copy of Barry's blogging software.
3. My GitHub username is patclaffey, this means my personal web-site repository must be called patclaffey.github.io -
 following GitHubs yourusername.github.io web-site naming convention.
4. I must rename my copy of the Jekyll Now repository to patclaffey.github.io.  
However I already had a repository of this name - so I just renamed the old repository to a different name.
This allowed my to successfully rename my Jekyll Now repository to patclaffey.github.io.
5. I opened a browser and entered the url http://patclaffey.github.io.   I now had a public blogging web-site.  That was really easy.  Thanks Barry!!

##Installing a local copy of "Jekyll Now" on Windows PC

1. As a GitHub user I already have the git tool installed on my desktop.  I cloned the patclaffey.github.io repository to my desktop.
Now I had local desktop access to all the pages that comprise my new web-site.
2. I went to the root directory of patclaffey.github.io on my desktop.
I ran Jekyll from here, to build the local copy of my web-site by running the following command:
    bundle exec jekyll server   
I could now access the local desktop copy of my Jekyll web-site at the url [http://localhost:4000](http://localhost:4000)  on my desktop browser. 

##Conclusions
It is really easy to install Barry Clark's Blogging Application.  This is a great software to get started blogging on GitHub.

{% comment %}

##Updating the "Jekyll Now" Configuration file
1. I changed my website’s name, description, avatar and other options by editing the local copy of _config.yml file.
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


you have to set up a local development environment, install dependencies and figure out Jekyll’s build process.
{% endcomment %}









