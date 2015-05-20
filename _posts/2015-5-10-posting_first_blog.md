---
layout: post
title: Posting my First Blog on GitHub
---
This blog is a work in progress.  The topic for this post is on posting a blog.


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









