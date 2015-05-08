---
layout: post
title: GitHub Web and Blogging Site Setup
---

This is my first blog on my new GitHub hosted web-site.  What will I write my first blog about?
I think its fair game to write about my experience setting up a new blogging web-site on GitHub.

As a GitHub user you can get one free static web-site.  They also provide a lean agile web development framework called Jekyll for maintaining the website.
An additional incentive from GitHub is they supply a cool personal website url - my url is http://patclaffey.github.io

Setting up the web site was easy.
Setting up Jekyll on the desktop was a time consuming and frustrating process.
This blog focuses on the trials and tribulations of setting up Jekyll on a Windows PC.
The issue is that many people will not persevere and spend many hours figuring out how to fix Jekyll installation issues.
This is a shame, because my experience of Jekyll is that it is a fantastic tool.
This blog was written using Jekyll on my local desktop.

{% comment %}
![_config.yml]({{ site.baseurl }}/images/config.png)  
For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.
{% endcomment %}

##Setting up a Personal Web-Site on GitHub
This is the easy part.  GitHub provide clear [instructions for setting up a user web-site]( https://pages.github.com/ ).  A user web-site is created in a GitHub repository with the naming convention username.github.io - in my case patclaffey.github.io.  To test the web-site you need to upload a simple "Hello World" index.html file.
 The test file can be created with the command -  echo "Hello World" > index.html.
 I opened my browser at my personal url patclaffey.github.io - and success, "Hello World" was displayed in the browser.
 
##Setting up Jekyll on a Desktop
This is the challenging part.  Here are the steps I followed to install Jekyll on my Windows 7 PC

1. Install Ruby on the PC
2. Install Ruby Development-Kit on the PC
3. Install Gem Bundler
4. Setup the file named Gemfile
5. Install Jekyll
6. Fix the windows hittimes bug
7. Run the Jekyll server

###Installing Ruby on a Windows PC
The first step in installing Jekyll is to installing the Ruby programming language.
This is needed because Jekyll is coded in Ruby.
Here is how I installed Ruby on my Windows desktop.

1. Download the Ruby code for Windows from [RubyInstaller for Windows]( http://rubyinstaller.org/downloads/)
2. I choose ruby 2.2.2 on top left hand side of page.
Note that this is the 32-bit version of Ruby.  The page advises to use 32-bit version on windows.
3. I had no issues installing ruby 2.2.2 on my PC.  From the installer choose the option to "Add Ruby executables to your PATH" - this is important.

###Installing Ruby Development-Kit on a Windows PC
This mandatory step is missing from the ["GitHub Jekyll setup page"](https://help.github.com/articles/using-jekyll-with-pages/).

1. Download the Ruby Development-Kit from [RubyInstaller for Windows]( http://rubyinstaller.org/downloads/)
2. I choose the development kit from bottom left hand side of screen.
I selected the development kit labelled "For use with Ruby 2.0 and 2.1 (32bits version only)".
3. The development kit is packaged as a 7-Zip archive.  The next step is to extract the development kit into an installation folder of your choice - I gave 7-Zip the folder name rubydev in the downloads folder.
4. Here are the instructions to [install the Ruby development kit](https://github.com/oneclick/rubyinstaller/wiki/Development-Kit).
   -  open a Windows Command line window 
   -  navigate to the installation folder you specified above - in my case "cd rubydev".
   -  run the command "ruby dk.rb init"
   -  next run the command "ruby dk.rb install"
5. Assuming above runs without error you have completed the install of ruby and the development kit.

###Install Gem Bundler
Bundler is a package manager that makes versioning Ruby software like Jekyll a lot easier.
To install Bundler, run the command "gem install bundle".  This command should without any errors, provided that Gemfile is setup correctly.


###Setup the file called Gemfile
The file called Gemfile is required in the root directory of the web-site repository - in my case the patclaffey.github.io repository.
The GitHub installation instruction page called ["Using Jekyll with Pages"](https://help.github.com/articles/using-jekyll-with-pages/) gives incorrect
instructions for this file.  The GitHub instructions are to create Gemfile with a single line as follows:    
gem 'github-pages'   

If Gemfile is created as above then the next step (Jekyll installation) fails with the following error:     
![Jekyll Install Error](/images/jekyll_install_error.PNG)

The fix for this Jekyll installation error is to create Gemfile with the following two lines:     
source 'https://rubygems.org'   
gem 'github-pages'   


###Install Jekyll
To install Jekyll, run the command "bundle install".  This command should without any errors, provided that Gemfile is setup correctly.
 
###Fix Hitimes Require Error  (Windows Ruby 2.2 Issue)
   
The command to run the Jekyll Server (from repository root directory) is :    
bundle exec jekyll server    

On Windows, when using Ruby 2.2,  this results in the following Hitimes Require Error.

![Jekyll Run Error](/images/jekyll_run_error.PNG)
 
The fix for this error is described in StackOverflow article ["Hitimes Require Error when running Jekyll serve on windows"]
(http://stackoverflow.com/questions/28985481/hitimes-require-error-when-running-jekyll-serve-on-windows-8-1).
 
###Running the Jekyll Server
The command to run the Jekyll Server (from repository root directory) is :      
bundle exec jekyll server    

Here is output from this command on my PC:   
![Jekyll Run Error](/images/jekyll_run.PNG)
 

I can view the output served by Jekyll in my desktop browser at the url http://localhost:4000





