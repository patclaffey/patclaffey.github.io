---
layout: post
title: Posting my First Blog on GitHub
---
My original idea was to write the first blog on this web-site about my experience of writing a blog.
Like all the best laid plans of men and mice - that did not happen.
In fact the first four blogs are about setting up a blogging site on GitHub.
Now at last here in the *fifth* blog, (yes Sir, Blog Number 5) describes the actual experience of writing a blog on GitHub.
I think the most powerful feature of blogging on GitHub is the simplicity of the blogging work-flow.
This work-flow lets the blogger focus on writing the blog content
and greatly simplifies the process of turning this writing into a good looking blog. 

##How to Create a new GitHub Blog
The assumption is that a GitHub blogger is familiar with the Git client and with using GitHub as a central repository.
The GitHub blogger will expect to follow the same work-flow for blogging as they follow for coding.
So the blogging process starts on the local server where they have their Git client.
New blog content is tested on the local Desktop.
When the blogger is happy with the blog they push the blog to their GitHub account to publish on the internet.

### Create a New Text File for the Blog
Each blog on GitHub is a separate text file, blogging starts by creating a new text file
on your desktop using your favorite desktop text editor.

### Save and Name this new Blog File
These text files are stored in the \_posts directory under the root directory of the web-site repository.
The text file name must start with the date, followed by subject and given the file extension ".md" which stands for MarkDown.
For example the file name for this blog is "2015-5-10-posting\_first\_blog.md"

### Add the Front Matter to the Blog File
The first section of the file is called the front matter - it is generally only a few lines in length.
The start of the front matter is identified by a line containing three dashes ( --- ),
as is end of the front matter.
In between these two lines an additional two lines are added.
The first additional line is the layout line which uses the the keyword  "layout:" and identify the css format file to include.
The second additional line is the title line which uses the the keyword  "title:" and is the web page title.


Here is the front matter (first four lines) of my first blog:     
    ---    
     layout: post    
     title: Setting up a Web Site and Blogging Site on GitHub    
    ---     
Note that title is front matter does not have to match the title in the blog text file name,
The title in front matter appears on the web as the title of the blog post.
### Add the Content to the Blog File
The content of the blog is added after the front matter.
Just start typing text - this text becomes the body of your blog.
Creating a new paragraph is easy - a single blank line identifies the end of one paragraph and the start of the next.
### Use MarkDown to enrich and format the Blog
The actual posts are written as text files and formatted using a convention called Markdown.
Markdown is very intuitive and quick to learn.
I use these [Markdown cheat sheets as a quick primer](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) on writing in Markdown.
The real power of Jekyll is its ability to generate web-sites from text files container Markdown.
The benefit of Markdown is that it lets you can focus on writing your content, greatly simplifying the formatting of the content.

### Test the Blog using Jeckyl on the local server

### Push Blog to GitHub to deploy on Internet

##Conclusion
I am familiar with using GitHub to develop and maintain software projects.
As a GitHub blogger I can use the work-flow I am familiar with as a software developer to maintain my blogging web-site.
As a blogger I am a writer in my native language.
In addition to writing I need to take of the formating of my writing.
The GitHub blogging needs to learn and become expert in the MarkDown protocol.
I have been quite happy to learn MarkDown - I cannot imagine any easier and more intuitive way of formating text files.
Looks like my experience of using MarkDown will be the subject of a future blog.










{% comment %}
you have to set up a local development environment, install dependencies and figure out Jekyll’s build process.
{% endcomment %}









