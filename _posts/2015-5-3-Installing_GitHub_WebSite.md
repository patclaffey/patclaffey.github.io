---
layout: post
title: Setting up a Vanilla Personal WebSite on GitHub
---
I want to setup a web and blogging site.
As a current GitHub user the idea of a GitHub hosted web-site is attractive to me.
GitHub provide one static personal web-site per user - and its free.
Also you get a cool personalized web-site url - in my case the url is [patclaffey.github.io]( http://patclaffey.github.io)

##How to Set-up a Personal Web-Site on GitHub
GitHub provide very clear [instructions for setting up a personal web-site]( https://pages.github.com/ ).
Just follow GitHub's instructions - its as easy as falling off a log.
To summarize - a GitHub web-site is created by setting up a GitHub repository with the naming convention username.github.io - in my case patclaffey.github.io.

A GitHub web-site in installed in a normal GitHub repository - the only thing that identifies it to GitHub as a web-site is the repository naming convention.
The web-site content is maintained like any other GitHub content by cloning to a local machine, making changes locally and then pushing the changes to GitHub.
This is standard GitHub workflow.

##How to Test the Web-Site
GitHub setup instructions advise testing the web-site installation using the familiar "Hello World" approach.
Navigate to the root directory of the web-site repository and issue the following command:

    echo "Hello World" > index.html
    
This creates the index.html file in the web-site root directory - the index.html file is the file rendered by web-site url.

I opened my browser at my personal url [patclaffey.github.io] ( http://patclaffey.github.io) - and success, "Hello World" was displayed in the browser.


##How does a GitHub Web-Site Work?
GitHub call their web-site technology GitHub Pages.
GitHub Pages uses a tool called Jekyll to read the user's web content from the web-site repository and generate the web-site on the internet.
The key technology used by GitHub Pages to generate the user web-site is Jekyll.



##Conclusion
There are a number of stages involved in setting up a GitHub web-site.
The first stage of the process, described in this blog, provisions a "Hello World" web-site and proving that the personal GitHub url is live on the Internet.
However after this step I still do not have a functional web-site.

A GitHub web-site is generated using the Jekyll tool which was used in this blog to render the "Hello World" page on the internet.
The next stage is to install Jekyll on the local Desktop.
This local installation is necessary so that the web-site can be generated and tested locally in private before deploying to the public over the Internet.
