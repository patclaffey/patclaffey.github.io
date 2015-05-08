---
layout: post
title: GitHub Web and Blogging Site Setup
---

This is my first blog on my new GitHub hosted web-site.  What will I write my first blog about?  I think its fair game to write about my experience setting up a new blogging web-site on GitHub.

As a GitHub user you can get one free static web-site.  They also provide a lean agile web development framework called Jekyll for maintaining the website.
An additional incentive from GitHub is they supply a cool personal website url - my url is http://patclaffey.github.io

Setting up the web site was easy.
Setting up Jekyll on my desktop this a time consuming and frustrating process.
This blog focuses on the trials and tribulations of setting up Jekyll on a Windows PC.
The issue is that many people will not persevere and spend many hours on Jekyll setup as I had to.
This is a shame, because my experience of Jekyll is that it is a fantastic tool.
This blog is written using Jekyll - and proof that the installation pain, though regrettable, is well worth it.
{% comment %}
![_config.yml]({{ site.baseurl }}/images/config.png)  
For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.
{% endcomment %}

##Instructions from GitHub on Setting up a Personal Web-Site
GitHub provide clear [instructions for setting up a user web-site]( https://pages.github.com/ ).  A user web-site is created in a GitHub repository with the naming convention username.github.io - in my case patclaffey.github.io.  To test the web-site you need to upload a simple "Hello World" index.html file.
 The test file can be created with the command -  echo "Hello World" > index.html.
 I opened my browser at my personal url patclaffey.github.io - and success, "Hello World" was displayed in the browser.

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

###Setup Gem Bundler
Bundler is a package manager that makes versioning Ruby software like Jekyll a lot easier.
To install Bundler, run the command "gem install bundle".  This command should without any errors, provided that Gemfile is setup correctly.


###Create the file called Gemfile
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
 
 
###Running the Jekyll Server
   
The command to run the Jekyll Server is :    
bundle exec jekyll server    
This command is run from the repository root directory.

On Windows this results in the following error:
![Jekyll Run Error](/images/jekyll_run_error.PNG)
 
The fix for this error is available from StackOverflow.



