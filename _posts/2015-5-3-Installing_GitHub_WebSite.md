---
layout: post
title: Creating a Personal WebSite on GitHub
---
I want to create a personal web and blogging site.
As a GitHub user the idea of a GitHub hosted web-site is attractive to me.
GitHub provide one static personal web-site per user - and its free.
Also you get a cool personalized web-site url - in my case the url is [patclaffey.github.io]( http://patclaffey.github.io)

GitHub provide very clear [instructions for setting up a personal web-site]( https://pages.github.com/ ).
Just follow GitHub's instructions - its as easy as falling off a log.
To summarize - logon to your GitHub account, create a new repository there,
name this new repository using the naming convention username.github.io - in my case patclaffey.github.io.
That's it - you now have a new GitHub hosted web-site.

##How to Test the Web-Site
Clone the web-site to your local machine - this is familiar work-flow for a GitHub user.
Navigate to the root directory of the web-site repository and create the site index file by issuing the following command:

    echo "Hello World" > index.html
    
Push these changes to GitHub.
The contents this site index file should get displayed on a browser at my personal GitHub web-site url.

I opened my browser at my personal url [patclaffey.github.io] ( http://patclaffey.github.io) - and success, "Hello World" is displayed in the browser.


##How does a GitHub Web-Site Work?
GitHub call their web-site technology GitHub Pages.
GitHub Pages use the tool called Jekyll to read the user's repository content and generate the web-site on the internet.
Jekyll is the key technology used by GitHub Pages to generate the user web-site.



##Conclusion
For a GitHub user creating a GitHub web-site is very easy.
However a web-site that only displays "Hello World" cannot be termed a functional web-site.
More software must be installed and configured before we can start blogging.
According to GitHub the next step is to install Jekyll on the local Desktop.

