---
layout: post
title: Running Jupyter Notebook in a Docker Container
updated: September 28, 2015
---
# Docker Hub
Today I registered my user name `patclaffey` on the [Docker Hub](https://hub.docker.com/) web-site - now I am a Docker Hub user.  On Docker Hub I naviaged to the `Dashboard` tab.  From here I pressed the `Create Repository +` button. The Create Repository dialog is as follows:

1. Choose a namespace (Required)  -  this defaults to `patclaffey`, my user-name
2. Choose a name (Required)  - I choose `jupyter_pandas` as my repository name
3. Add a short description (Required) - I added a short description
4. Add markdown to the full description field  - I left this blank initially, and filled this field in later
5. Set it to be a private or public repository  - I left this as `public`, the default value.

Thats all there is to creating a new Docker Hub repository on the web-site. 
 The next step is to push an image to the repository.  The next step is to create the image with the correct naming convention in Docker.  The naming convention is user_name/reporitory_name:tag.  Here is the command I used:
```
docker build - t "patclaffey/jupyter_pandas:v2" 
```

Next simple use the `docker push` command to push the image to Docker Hub:
```
docker push patclaffey/jupyter_pandas:v2
```

I then went back toi my browser and naviaged to  Docker Hub.  I went to the Dashboard tab and in the Tags sub-tab I could see the `v1` image. 
