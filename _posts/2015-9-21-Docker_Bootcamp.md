---
layout: post
title: Docker Bootcamp
updated: September 28, 2015
---
I attended the Docker Hackaton organized by Demonware on the 19th Sept 2015 in Dublin.  The Hackaton was run as part of the Global Docker hacking weekend.  Our hosts / guides for the day were Tom and Nic from DemonWare.  The event took place in the WorkDay building in SmithField.  Thanks to WorkDay for providing the venue and Softlayer for the food and beverages.

My goal, as a Docker newbee,  was to learn what the buzz about Docker was all about.  My first decision was whether to learn Docker through Windows 7 or Ubuntu Linux - my PC has both operating systems installed.  I decided to learn through Lunux - so I booted my laptop up with Ubuntu.  My first of many pleasant surprises was the speed and ease the Docker install process.  There were two steps, first an apt-get command to setup Docker on my laptop.  The second step was to add my PC user to a new host Linux group using the Linux useradd command.  That was it.  I was up and running with Docker. From the get go I was getting a really positive impression of Docker.

As regards learning Docker - this was another pleasant surprise.  DemonWare had a 40 page document called Docker Bootcamp.  To learn Docker I just had to fall in to the DemonWare bootcamp.  And any time I got stuck I just had to call on the bootcamp NCOs Nic and Tom and they put me on the right path.

There appear to be two key Docker concepts for the newbee to grapple with - the **image** and the **container**.  You start with an image.  The image is a composite object - the most import part of the image is the image base.  The image base will become the containers OS - for the bootcamp this was Ubuntu 14.04.  The image is built up in software layers on top of the image base.  A Docker container is then created by running an image. A Docker container is like a virtual computer and behaves like a stand-alone computer.  Docker containers are incredibly light-weight, so by creating lots of containers you turn a single host computer into a full fleet of computers. Each of these Docker containers can run its own OS and its own software modules independent of each other and the host.

The Docker commands are really powerful and intuitive.  For example to get information on your Docker images just type `docker images`.  To find out about your Docker containers type `docker ps`.  There are buckets of other commands and cool things to do - just check the Docker documentation.

The food was excellent at the event.  I got two tee-shirts.  I wore the red Docker Hackaton tee-shirt home : my daughter eyed it enviously and said it was too cool for me.  She immediately requisitioned the really cool DemonWare tee-shirt, and gave her approval to its American Apparel label.  A few of us made it to the Brazen Head for some Guinness and fake craft beer.  

T.I.L. or Today I Learned Docker.  Awesome - I cant wait to start using it.   
