---
layout: post
title: My Docker Road Map 
---


Since completing the [DemonWare Docker Bootcamp](http://patclaffey.github.io/Docker_Bootcamp/), I have become a Docker user.  I am now doing all my software development under Docker - see my Jupyter Pandas responsitory on [GitHub](https://github.com/patclaffey/docker_jupyter).  I have also released my Jupyter Docker Image on [Docker Hub](https://hub.docker.com/r/patclaffey/jupyter_pandas/).

I am now consolidating the Docker fundamentals that I have learned.
I am considering the Docker road ahead of me, what I still need to learn - my personal Docker Road Map.



## My Use Case

My use case is to investigate the use of Docker within the Python eco-system.  In my opinion the existing Python tools for virtualization are weak.  Docker may provide a better alternative.  My first use of Docker has been to containerize the popular Jupyter Notebook running Python 3.



## Docker Fundamentals

In my experience, the fundamentals of Docker revolve around building images and running containers.

### Building a Docker Image

The image is a fundamental building block in Docker.  Docker allows you to create your own images tailored to your own needs.  An image consists of a base image with additional software components added on top.  At the moment the base image must be a linux kernel - I use Ubuntu 14.04, but there are many more to choose from.
After the base image is decided on you can add  additional software such as: software packages from public or proprietary distributions,  additional files or code that you develop yourself for your use case.
The image allows you to create your own software stack.
        
The core artifact for building an image is the Dockerfile containing Dockerfile Instructions.  Docker have documented these instructions in the [Dockerfile Reference](https://docs.docker.com/reference/builder/)  - here are some examples of the most commonly used:

- **FROM** - adds the base image to the file, and must be first instruction in Dockerfile 
- **MAINTAINER** - name and email address of image maintainer
- **RUN** - runs OS commands as part of image build process for example to download and install software packages from repositories.
- **ENV** - sets up and environment variable in the image
- **ADD** or **COPY** - copies files into image
- **ENTRYPOINT** or **CMD** - the default OS command or program that runs when a new container that runs this image starts 
- **EXPOSE** - expose a port to host

A number of Docker commands are used all the time with images- see [Getting Started with Docker Images](https://docs.docker.com/userguide/dockerimages/).  Here are some of the most commonly used:

- `docker build` - this is one of the the most important Docker commands.  It reads the Dockerfile and actually builds the docker image
- `docker images` - list docker images
- `docker rmi` - delete docker images

Dockerfile is not the only way to build an image- but is a best practice and a fundamental approach to defining images and understanding Docker.

### Buiding a Container
The container is fundamental to and epitomizes Docker. The container is how Docker implements virtualization - a container behaves like a vitual linux computer.  Docker acts as the engine for running one or more containers on a host computer.

Containers are created from images using the `docker run` command, so this is a very important docker command and is documented in the [Docker run reference](https://docs.docker.com/reference/run/).  The  `docker run` command has a number of arguments, here are some of the most important:

- **image name**  :  the image defines the operating system and software stack that runs in the container.
- **-d**  :  run the container in disconnected mode
- **-i**  :  run the container in interactive mode
- **-t**  :  stream container output to screen (tty) 
- **-name**  : given name for container
- **-v**  :  map a volume from host to container (multiple -v arguments can be supplied)
- **-p**  :  map a port between container and host

Some of the common commands for use with docker containers are

- `docker run` - create and run a container
- `docker ps`  - list running containers
- `docker rm`  - delete a container
- `docker start`  - start a container
- `docker stop`  - stop a container


   

## Docker Hub
[Docker Hub](https://hub.docker.com/) is a repository on the cloud for Docker Images.  You do not need a Docker Hub account to search or pull images from Docker Hub.  You can search Docker Hub from the Docker command line using the `docker search` command.  For example to search for Jupyter images type `docker search jupyter`.  You can download images from Docker Hub using `docker pull`, again without registering on Docker Hub.

The benefit of registering on Docker Hub is that it allows you to save your Docker images on the cloud.  These images can be saved in either public or private mode.  This makes it easy to distribute your images and also to move them between different hosts and devices.  The `docker pull` command is used to download an image from Docker Hub.
    

## Next Steps

### Getting Deeper Docker Knowledge

To move beyond the fundamentals I am looking for and reading more in-depth Docker articles.  I have found the [Innovation Lab Blogs](https://labs.ctl.io/blog/) very helpful.
For example the posting [Dockerfile ENTRYPOINT vs CMD](https://labs.ctl.io/dockerfile-entrypoint-vs-cmd/) by Brian DeHamer- he explains with clarity the subtleties of running commands and software at container startup.  By the same author is another excellent article [Gracefully Stopping Docker Containers](https://labs.ctl.io/gracefully-stopping-docker-containers/)

"The Docker Book" by James Turnbull contains a lot of useful information on complex Docker deployments. 

### Docker in the Python Eco-System
I am interested in using Docker within the Python eco-system.  As an example I have developed a Docker image and container for Jupyter. 
I want to understand the up-take of Docker within the Python community and plans for its future use.



### Docker and Windows
I am using Docker on linux hosts, AWS EC2 and laptop with Ubuntu. I would like to try Docker on a Windows environment

### Docker Eco-System
A number of tools are available within the Docker Eco-System.  They include

- Compose
- Machine
- Swarm
- Rancher

There is no shortage of things to learn in Docker.

## Conclusion
Docker is a technology I can apply to my Python development work.  This blog has been written in a application running in my Docker container. 
I would like to further investigate the potential of Docker to benefit the Python community, with Dockers superior virtualization and portability between environments and devices. 
Docker fits neatly with my interest in linux and study of linux system administration.
I am interested in progressing my Docker skills, moving beyond the Docker fundamentals, and learning the advanced Docker tools and techniques.
