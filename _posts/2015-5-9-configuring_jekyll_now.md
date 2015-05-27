---
layout: post
title: Customizing "Jekyll Now" Blogging Application
---


The Jekyll Now powered blogging site is customized by a configuration file.
This blog describes the customizations made to the blogging site using this configuration file.
In addition the contents of the About file needs to be updated for the user.

The site configuration file is called _config.yml.  It is found in the root directory of the web-site.
This file is a plain text file and can be edited using any text editor.

##Customizing the Blog Site Header
The blog site header is customized using the site configuration file.
###name
The name of the blogger is displayed at the top of every blog and web page in the site.
This is achieved by setting the value of the *name* field in the configuration file.
In my case I set the web site name to "Pat Claffey" by entering my name in the configuration file as follows:

    # Name of your site (displayed in the header)
    name: Pat Claffey


###description
A short bio or description of the blogger is displayed at the top of every blog and web page in the site.
This is achieved by setting the value of the *description* field in the configuration file as follows:

    # Short bio or description (displayed in the header)
    description: Experienced solution architect, Python Ireland company member.


###avatar
An avatar or photo of the blogger is displayed at the top of every blog and web page in the site.
This is achieved by setting the value of the *avatar* field in the configuration file as follows:

    # URL of your avatar or profile pic (you could use your GitHub profile pic)
    avatar: https://avatars1.githubusercontent.com/u/9211427?v=3&u=bc78925a4024a18cba3d184315ccdfd615d76413&s=140

	
##Customizing the Blog Site Footer
	
The social media icons at the foot of each web or bloke page are customized by
setting values for the foot-links fields in the configuration file.
In the case of this web-site, icons are enabled for email address,
GitHub, LinkedIn and Twitter by entering my details in the configuration file as follows:

    # Includes an icon in the footer for each username you enter
    footer-links:
      dribbble:
      email: patclaffey@gmail.com
      facebook:
      flickr:
      github: patclaffey
      instagram:
      linkedin: patclaffey
      pinterest:
      rss: # just type anything here for a working RSS icon, make sure you set the "url" above!
      twitter: patclaffey
      stackoverflow: # your stackoverflow profile, e.g. "users/50476/bart-kiers"
      youtube: # channel/<your_long_string> or user/<user-name>
      googleplus: # anything in your profile username that comes after plus.google.com/

	  
##Customizing the About File
The About File needed to be updated with my details.

##Pushing changes to GitHub
The above changes were tested on the local Desktop.
The local Jekyll server needs to stopped and then restarted to test configuration file changes.
The local server is restarted using the command:

    bundle exec jekyll server

Once the owner tests and verifies the changes on the local server they are pushed to GitHub to release to the Internet.

##Conclusions
It is quick and easy to customize Jekyll Now.  It is easy to edit the configuration file and About file.





{% comment %}
you have to set up a local development environment, install dependencies and figure out Jekyll’s build process.
{% endcomment %}









