---
layout: post
title: Using Docker Hub 
updated: September 28, 2015
---
Today I registered my user name `patclaffey` on the [Docker Hub](https://hub.docker.com/) web-site - I am now the proud owner of a personal [patclaffey Docker Hub](https://hub.docker.com/u/patclaffey/) account. 
The first thing I did on Docker Hub was create a public repository for my Jupyter / Pandas image.  I navigated to the `Dashboard` tab, pressed the `Create Repository +` button and followed its dialog:

1. Choose a namespace (Required)  -  defaults to my user name `patclaffey`
2. Choose a name (Required)  - I choose `jupyter_pandas` as my repository name
3. Add a short description (Required) - I added a short description
4. Add markdown to the full description field  - I left this blank initially, and filled this field in later
5. Set it to be a private or public repository  - I left this as `public`, the default value.

I now have the empty Docker Hub repository for my project. This is a repository for project Docker images. 
To add an image I need to leave Docker Hub and return to the docker tool on my host laptop.  

To use Docker Hub, the Images on the host must follow the Docker Hub naming convention.
This naming convention is user\_name/reporitory\_name:tag.  Here is the command I used to prepare the image prior to pushing it to Docker Hub:

```
docker build - t "patclaffey/jupyter_pandas:v2" 
```

The `docker push` command is used to push the image to Docker Hub:

```
docker push patclaffey/jupyter_pandas:v2
```

I navigated back to the Docker Hub dashboard on my browser.
I verified that my image was successfully loaded by going to the Tags sub-tab.
I verified that the image tagged `v2` was available 

## Benefits of Docker Hub
The major benefit of Docker Hub is that my image is now publically available to any user from any Docker host using the following `docker pull` command:

```
docker pull patclaffey/jupyter_pandas:v2
```

A more intangible benefit of Docker Hub is that by making the image public, it focuses the user on the quality of the image.  So that will be the subject of a follow on blog.  I would like to apply the Docker Hub image best practices to create the highest quality possible image for Jupyter and Pandas.
