---
layout: post
title: Setup of a GitHub Web and Blogging Site
---

This is my first blog on my new GitHub hosted web-site.  What will I write my first blog about?  I think its fair game to write about my experience setting up a new blogging web-site on GitHub.

As a GitHub user you can get one free static web-site.  The also provide a lean agile web development framework called Jekyll for maintaining the website.  An additional incentive from GitHub is they supply a cool personal website url - my url is http://patclaffey.github.io

{% comment %}
![_config.yml]({{ site.baseurl }}/images/config.png)  
For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.
{% endcomment %}
##Creating a GitHub Personal Web-Site
GitHub provide clear [instructions for setting up a user web-site]( https://pages.github.com/ ).  A user web-site is created in a GitHub repository with the naming convention username.github.io - in my case patclaffey.github.io.  To test the web-site you need to upload a simple "Hello World" index.html file.
 The test file can be created with the command -  echo "Hello World" > index.html.
 I opened my browser at my personal url patclaffey.github.io - and success, "Hello World" was displayed in the browser.

##Setting up Jekyll on your PC
GitHub recommends a tool called Jekyll for maintaining your web-site.
Jekyll takes text files with special commands called mark-down (yes "mark-down" and not "mark_up") and automatically formats web ready pages.
Jekyll will (hopefully) give me a great looking web-site and simplify web-site maintainence.

GitHub recommend that you install and setup Jekyll on your local desktop so that you can test your content locally before deploying to the web via GitHub.
GitHub provide [instructions on how to setup Jekyll](https://help.github.com/articles/using-jekyll-with-pages/).

1. The first instruction is to setup Ruby on your desktop.
What GitHub omit to say is that in addition to Ruby, you also need the Ruby Development Kit, because these are two separate installs.
I will give instructions on how I setup Ruby (and the associated Development Kit) on my PC, because I found this a bit painful.
2. The second instruction is to install Bundle.  This worked fine for me.
3. The third instruction is to install Jekyll.  When I did this the gemfile contents was incorrect (the "source" line was missing).
But this step appears to have been corrected now.

When I tried to run Jekyll it failed with a very unfriendly stack trace.  I will describe below how I fixed this error.
In the end I got Jekyll to run - and so far I think it is worth the effort.

###Installing Ruby and Ruby Development Kit on a Windows 7 PC
Here is how I installed both Ruby and the associated development kit on my Windows 7 Professional desktop:

1. The page to get Ruby code for Windows is called [RubyInstaller for Windows]( http://rubyinstaller.org/downloads/)
2. I choose ruby 2.2.2 on top left hand side of page.
Note that this is the 32 bit version of Ruby.  The page advises to use 32-bit version on windows.
3. I had no issues installing ruby 2.2.2 on my PC.  From the installer choose the option to "Add Ruby executables to your PATH" - this is important.
4. I choose the development kit from bottom left hand side of screen.
I selected the development kit labelled "For use with Ruby 2.0 and 2.1 (32bits version only)".
5. The development kit is packaged as a 7-Zip archive.  The next step is to extract the development kit into an installation folder of your choice - I gave 7-Zip the folder name rubydev in the downloads folder.
6. Here are the instructions to [install the Ruby development kit](https://github.com/oneclick/rubyinstaller/wiki/Development-Kit).
   -  open a Windows Command line window 
   -  navigate to the installation folder you specified above - in my case "cd rubydev".
   -  run the command "ruby dk.rb init"
   -  next run the command "ruby dk.rb install"
7. Assuming above runs without error you have completed the install of ruby and the development kit.
   
###Fixing the Ruby error and getting Jekyll to run 



