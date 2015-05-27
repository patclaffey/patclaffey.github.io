---
layout: post
title: Posting my First Blog on GitHub
updated: May 27, 2015
---
The original idea for my first blog was to write about my experience of writing my first GitHub blog.
Like the best laid plans of men and mice - that did not happen.
In fact the first four blogs are about setting up a blogging site on GitHub.
Now at last here in the *fifth* blog, (yes Madame, Blog Number 5) gets to the actual experience of writing a blog on GitHub.
I think the most powerful feature of blogging on GitHub is the simplicity of the blogging work-flow.
This work-flow lets the blogger focus on writing the blog content
and greatly simplifies the process of turning this writing into a blog. 

##How to Create a new GitHub Blog
As a software developer I am used to using Git and GitHub for managing software files as part of software projects.
The GitHub blogger can expect to follow a similar work-flow for blogging as for their software project.
This is because a GitHub bogging application is also managed as a collection of files in a GitHub repository.
However in addition to the GitHub type steps - there are also steps specific to using Jeckyl Now as the blogging software.
This section outlines the steps I follow, GitHub specific as well as Jeckyl Now specific, to write a blog.

{%  comment %}
The overall work-flow should look very familiar to the GitHub user.
I also detail the steps that are specific to blogging using Jeckyl Now.

This section details the steps I follow to write a blog.

The nice thing about using GitHub as a blogging platform is that GitHub skills are re-purposed for maintaining blog content.
The assumption is that a GitHub blogger is familiar with the Git client and with using GitHub as a central repository.
The GitHub blogger will expect to follow the same work-flow for blogging as they follow for coding.
So the blogging process starts on the local server where they have their Git client.
New blog content is tested on the local Desktop.
When the blogger is happy with the blog they push the blog to their GitHub account to publish on the internet.
{%  endcomment %}
### Create a New Text File for the Blog
The starting point for a new blog is creating a text file with your favorite text editor.
Following standard GitHub work-flow this file is created on your local machine - in my case my windows desktop.
Every blog gets its own text file.

### Follow Blog File Name Convention
All blog files for the Jekyll Now blogging application must follow its file name convention.
The file name starts with the blog date, followed by the blog description.
The file extension is .md (meaning a file containing MarkDown syntax).
For example the file name for this blog is "2015-5-10-posting\_first\_blog.md".

### Save the Blog Text File in \_posts directory
The blog file needs to be saved locally in the correct directory.
Navigate to the root directory for the GitHub web-site (username.github.io).
This directory should contain a \_posts directory created by the Jeckyl Now installation.
All blogs are saved in this \_posts directory.


### Add the Front Matter to the Blog File
The first few lines of the blog file is called the front matter - this section is mandatory.
The front matter starts and ends with a line containing three dashes ( --- ).
In between these lines two additional lines are added.
The first additional line starts with the keyword  "layout:" and links to a file in the \_layout that controls blog layout.
The second additional line starts with the keyword  "title:" and contains the title of the blog.


Here is the front matter (first four lines) for this blog:
   
    ---    
     layout: post    
     title: Posting my First Blog on GitHub    
    ---     
	
Note that the title in the front matter does not have to match the description in the blog file name.
The title in the front matter gets published as the blog title - it can be changed as required.

### Add the Content to the Blog File
The blog content is added after the front matter.
Just start typing text - the text you add becomes the body of your blog.
Creating a new paragraph is easy - a single blank line creates a new paragraph.
### Use MarkDown to enrich and format the Blog
A syntax called MarkDown is used to format the blog.
I found MarkDown very intuitive and quick to learn.
I use these [Markdown cheat sheets as a quick primer](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) on writing in Markdown.
The MarkDown syntax is what I like most about this blogging software,
its simplicity keeps the blogger's focus on writing.

### Pre-view the Blog on the local server
Writing a blog is a very interactive process.
Before publishing a blog, you must pre-view and check the content and layout many times.
This means it is very important to have Jeckyl installed correctly and running locally.
To run Jeckyl type the following command in the web-site root directory:

    bundle exec jekyll server

...and then open the desktop browser at the local Jeckyl url [http://localhost:4000](http://localhost:4000) to pre-view the blog.



### Publish the Blog
The final step is to publish the blog.  This is done, as per normal GitHub workflow, by pushing the local repository content to GitHub.
Once the latest content is live on the GitHub repository, GitHub takes care of generating your web-site.
The new blog is now available at your personal GitHub web url.


##Conclusion
I have now written five blogs about my GitHub blogging experience.
The most frustrating aspect was setting up Jeckyl on my Windows PC.
Jeckyl is the software that is required to pre-view blogs on the local machine before publishing to the web.
My best discovery was installing the Jeckyl Now Blogging application written by Barry Clark.
Barry's Jeckyl Now is like WordPress for GitHub - its the perfect starting point for GitHub blogging.
I like to simplicity of the blogging work-flow such as using text files and MarkDown syntax.
Once all the required software is installed I think that this will be a productive and fun way to blog.



{%  comment %}
I am familiar with using GitHub to develop and maintain software projects.
As a GitHub blogger I can use the work-flow I am familiar with as a software developer to maintain my blogging web-site.
As a blogger I am a writer in my native language.
In addition to writing I need to take of the formating of my writing.
The GitHub blogging needs to learn and become expert in the MarkDown protocol.
I have been quite happy to learn MarkDown - I cannot imagine any easier and more intuitive way of formating text files.
Looks like my experience of using MarkDown will be the subject of a future blog.
{%  endcomment %}









{% comment %}
you have to set up a local development environment, install dependencies and figure out Jekyll’s build process.
{% endcomment %}









