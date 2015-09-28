---
layout: post
title: Using Docker Hub 
updated: September 28, 2015
---
Today I registered my user name `patclaffey` on the [Docker Hub](https://hub.docker.com/) web-site - now I am a Docker Hub user. 
The first thing I needed to do in Docker Hub was to create a Docker Hub repository.  I navigated to the `Dashboard` tab.  From here I pressed the `Create Repository +` button and followed its dialog:

1. Choose a namespace (Required)  -  this defaults to `patclaffey`, my user-name
2. Choose a name (Required)  - I choose `jupyter_pandas` as my repository name
3. Add a short description (Required) - I added a short description
4. Add markdown to the full description field  - I left this blank initially, and filled this field in later
5. Set it to be a private or public repository  - I left this as `public`, the default value.

At this point I have a new empty Docker Hub repository - next step is to add content to the repository which is the a 
Docker image.

Images are pushed to the repository from the Docker tool on the host system.  The image must be created on the host with the correct naming convention.  The naming convention is user\_name/reporitory\_name:tag.  Here is the command I used:
```
docker build - t "patclaffey/jupyter_pandas:v1" 
```

Finally use the `docker push` command to push the image to Docker Hub:
```
docker push patclaffey/jupyter_pandas:v1
```

I then went back to my browser and navigated to Docker Hub.  I went to the Dashboard tab and in the Tags sub-tab I could see the `v1` image. 
