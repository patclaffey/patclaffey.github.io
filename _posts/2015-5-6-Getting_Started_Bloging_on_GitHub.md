---
layout: post
title: Installing and Running Jekyll on Windows
---
GitHub call their web-site technology GitHub Pages.
GitHub Pages uses a web framework called Jekyll.
Jekyll is a free open source product from the ruby programming community.
Jekyll takes the user's content and transforms it into web pages for display in a browser.
GitHub advise that the user should install Jekyll on their local machine.
This local Jekyll installation allows the user to test their web-site before release to the world wide web.

 
##Overview of Jekyll Installation Steps
The page ["Using Jekyll with Pages"](https://help.github.com/articles/using-jekyll-with-pages/) from GitHub
is the guide for installing Jekyll for use with GitHub web-site.
There is a lot of really useful information in this page, including good information on external Jekyll resources.
However, it is still a struggle to install Jekyll locally on Windows.
This installation is hard - my concern is that most users will have neither the time, skill or patience to tackle this task.

The strength of open source is the capability, which Jekyll illustrates, to create something powerful by combining other open source products.
These multiple dependencies can make installation painful.
The goal of this blog is to help others who want to install Jekyll on Windows,
and also to suggest areas of improvement in the installation process.
My main finding is that the issue is less a software problem than a documentation issue.



The steps I followed to install Jekyll on my Windows 7 PC are as follows:

1. Install Ruby on Windows
2. Download Ruby Development-Kit on Windows
3. Install Ruby Development-Kit on Windows
4. Install Gem Bundler
5. Setup the file named Gemfile
6. Install Jekyll
7. Fix the windows hittimes bug
8. Run the Jekyll server

 

###Installing Ruby on a Windows PC
The first step in installing Jekyll is to install the Ruby programming language.
This is needed because Jekyll is coded in Ruby.
Here is how I installed Ruby on my Windows desktop.

1. Navigate to the Ruby page for Windows: [RubyInstaller for Windows]( http://rubyinstaller.org/downloads/)
2. There is a choice of three versions of Ruby to download - I choose the latest version.
This is Ruby 2.2.2 - see link on top left hand side of page.
Note that this is the 32-bit version of Ruby.  The page advises to use 32-bit version on windows.
3. I had no issues installing Ruby 2.2.2 on my PC.  From the installer options it is important to choose the option to "Add Ruby executables to your PATH".

I find the Ruby Windows download page cluttered and confusing.  I expected a page with a big button labelled "Download Latest".
Instead to my surprise I had to decide which of seven available Ruby versions I should choose.


###Installing Ruby Development-Kit on a Windows PC
This mandatory step is missing from the ["GitHub Jekyll setup page"](https://help.github.com/articles/using-jekyll-with-pages/).

1. Navigate to the Ruby page for Windows: [RubyInstaller for Windows]( http://rubyinstaller.org/downloads/)
2. I choose the development kit from bottom left hand side of screen.
I selected the development kit labelled "For use with Ruby 2.0 and 2.1 (32bits version only)".
3. The development kit is packaged as a 7-Zip archive.  
The next step is to extract the development kit into a Windows folder - I extracted the kit into a new folder downloads\rubydev


###Installing Ruby Development-Kit on a Windows PC
This mandatory step is missing from the ["GitHub Jekyll setup page"](https://help.github.com/articles/using-jekyll-with-pages/).

1. You need to navigate to a new Ruby web page to for the instructions to [install the Ruby development kit](https://github.com/oneclick/rubyinstaller/wiki/Development-Kit).
2. Here is how I installed the Ruby Development kit:
   -  open a Windows Command line window 
   -  navigate to the installation folder specified above - in my case "cd downloads\rubydev".
3. run the following commands:

    ruby dk.rb init    
    ruby dk.rb install    
    
The above commands ran without error -  this completed the install of Ruby and the development kit.

The Ruby Windows page contains the link for downloading the Development-Kit - but no instructions on on to install it.
I had to use Google to find these install instructions.

###Install Gem Bundler
Bundler is a package manager that makes versioning Ruby software like Jekyll a lot easier.
To install Bundler, run the command:

    gem install bundle
This command ran without any errors.


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
To install Jekyll, run the command:
    bundle install
This command should without any errors, provided that Gemfile is setup correctly.
 
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
 

I can view the output served by Jekyll in my desktop browser at the url [http://localhost:4000](http://localhost:4000)


##Conclusions
The instructions in the page ["Using Jekyll with Pages"](https://help.github.com/articles/using-jekyll-with-pages/) from GitHub completely
underestimates the difficulty of installing Jekyll.  The page says that this installation is easy - this is certainly not my experience.
The page should add instruction about downloading and installing the Ruby Development-Kit.
It should also give crystal clear instructions on the contents of Gemfile.

The Ruby Community should simplify and clarify the instructions for installing Ruby and the Ruby Development-Kit on Windows.

The Ruby Windows Hittimes bug should be fixed - this is the only software related issue found in this install.



