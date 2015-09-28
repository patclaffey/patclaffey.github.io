---
layout: post
title: Using Docker Hub 
updated: September 28, 2015
---
Today I registered my user name `patclaffey` on the [Docker Hub](https://hub.docker.com/) web-site - I am now a Docker Hub user. 
The first thing I needed in Docker Hub was a repository.  I navigated to the `Dashboard` tab, pressed the `Create Repository +` button and followed its dialog:

1. Choose a namespace (Required)  -  this defaults to `patclaffey`, my user-name
2. Choose a name (Required)  - I choose `jupyter_pandas` as my repository name
3. Add a short description (Required) - I added a short description
4. Add markdown to the full description field  - I left this blank initially, and filled this field in later
5. Set it to be a private or public repository  - I left this as `public`, the default value.

I now have an empty Docker Hub repository. Content needs to be added to repository, this content are the Docker images.

Images are pushed to the repository from the Docker tool on the host system. 
Imageis must be named on the host with the correct naming convention.  The naming convention is user\_name/reporitory\_name:tag.  Here is the command I used:
```
docker build - t "patclaffey/jupyter_pandas:v1" 
```

The `docker push` command is used to push the image to Docker Hub:
```
docker push patclaffey/jupyter_pandas:v1
```

From my browser I navigated to Docker Hub.  I went to the Dashboard tab and in the Tags sub-tab I could see the `v1` image. 
