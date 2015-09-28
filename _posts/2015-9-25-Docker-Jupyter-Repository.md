---
layout: post
title: Running Jupyter Notebook in a Docker Container
updated: September 28, 2015
---

I have created a new GitHub [Docker Jupyter repository](https://github.com/patclaffey/docker_jupyter) in my personal GitHub account. The repository contains the code to run the latest version of Jupyter (using version 4.0 documents) on Ubuntu 14.04 in a Docker Container.  I have tested this Docker container on my PC (using Ubuntu 14.10) and also on the cloud (using an AWS EC2 instance with Red Hat Linux).  I verified that I could work successfully with the Jupyter Notebook content over the cloud.

Since finishing the DemonWare Bootcamp on Docker run by Tom and Nic I have been stuck into Docker. 
The issue with working with Python and open source tools such as Jupyter is that these tools are under constant development and change.
Almost every new project involves a new software build because software at every level of the stack is in constant flux.
The result of this constant change has been chaos as the vast majority of software builds cannot be tracked.
The beauty of Docker is it gives control over the software build process.
Now I can efficiently and effectively track, understand, port and manage  my software builds.

The Jupyter Notebook is a web application that allows you to create and share documents that contain live code, equations, visualizations and explanatory text.  I am interested in Jupyter because it provides a great front-end for Python development, data analysis and visualization.  I am using it to analyze personal activity information from sources such as Garmin, Strava, FitBit and Track My Ride.  The public web-sites for these companies never give me the analysis I want.  So I am using the power of Jupyter and Python to analyze this information. Given the importance of individual activity in health, fitness, tackling obesity - I am hoping there will be sufficient interest to open source this work.

The GitHub [Docker Jupyter repository](https://github.com/patclaffey/docker_jupyter) contains the code and also full instructions on how to run Jupyter in Docker. Here is an overview of the install steps:  

*  clone  [Docker Jupyter repository](https://github.com/patclaffey/docker_jupyter) to your local host  
*  add public key file named mycert.pem (instructions provided)  
*  run the script to build the project docker image  
*  run the script to create and start the Docker Container  
*  logon to Jupyter and view the sample notebook  

My experience is that Jupyter runs flawlessly in Docker on my laptop and also on AWS EC2.  With Docker I now have complete control over my full software stack. I can spin as many instances of my stack as I require. Also I can port and share my software with ease.  I can run the same software on my laptop and on the cloud.
