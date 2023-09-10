# Docker

<p>
    <img src="https://upload.wikimedia.org/wikipedia/commons/7/79/Docker_%28container_engine%29_logo.png?20150121160542" alt="Docker Logo" height="260">
</p>

# Contents

1. [Introduction](#introduction)
2. [Setup Docker](#setupdocker)

- Install Docker on Ubuntu

```js
   sudo apt-get update

   sudo apt-get install ca-certificates curl gnupg

   sudo install -m 0755 -d /etc/apt/keyrings

   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
    
    sudo chmod a+r /etc/apt/keyrings/docker.gpg
    echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  
  sudo apt-get update
  
  sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

3. [Creating and Using Containers](#containers)
   - Command format
     ```js
     docker management_command sub_command options
     ```
   - image vs Container
     - image - application we want to learn.
     - container - instance of image, many containers can be created from same
       image.
   - Creating ngix server
     ```js
     docker container run -p 80:80 nginx
     ```
     1. Pulls image from Docker Hub if not present on local machine.
     2. Runs image.
     3. Open up port 80 for requests.
   - Running docker in background
     - option --detach going to help us to run docker image in background.
   ```js
   docker container run -p 80:80 --detach nginx
   ```
   - Listing Docker Container
     - ls sub-command going to help in listing docker container.
     ```js
     docker container ls
     ```
     Each Docker container have its unique docker id and docker name (if not
     provided).
   - Stopping Docker container
     - stop subcommand going help us to stop docker container.
     ```js
     docker container stop containerid
     ```
   - Naming docker container
   - using --name options we can provide name to docker container.
   ```js
   docker container run -p 80:80 --detach --name nginx-server nginx
   ```
   1. We are checking if image locally exists, if not pull from Docker hub.
   2. Run image.
   3. Open port 80 to handle request.
   4. Run in background mode. (--detach)
   5. Name it as nginx-server. (--name)
   - Listing all Running and non running Container.
   - option -a going to help us to list out all running and stopped container
     list.
   ```js
   docker container ls -a
   ```
   - Removing all Container at once
     - Sub command rm going to help us to remove all containers at once
     ```js
     docker container rm container_id1 or name1 container_id2 or name2 container_id3 or name3
     ```
4. [Building and Finding Container images](#containerimages)
5. [Persistent Data : Volumes](#volumes)
6. [Docker Compose](#dockercompose)
7. [Swarm Introduction](#swarmintroduction)
8. [Swarm Features](#swarmfeatures)
9. [Swarm Lifecycle](#swarmlifecycle)
10. [Container Registries and Image storage and distribution](#containerregistries)
11. [Docker in Production](#dockerinproduction)
12. [The kubernetes](#kubernetes)
13. [Kubernetes Architecture and Install](#architectureandinstall)
14. [Your first pod](#pod)
15. [Inspecting Kubernetes Resources](#inspectingresources)
16. [exposing Kubernetes Ports](#exposingports)
17. [Kubernetes Management Techinques](#managementtechiqueskubernetes)
18. [Kubernetes YAML](#kubernetesyaml)
19. [Future of Kubernetes](#futureofkubernetes)
20. [Automated CI Workflows](#automatedci)
21. [Gitub Actions](#githubactions)
22. [Docker Security: Default and Tools](#dockerseucitytools)
23. [Docker 19.03 New Features](#newfeaturesdocker)
24. [DevOps and Docker](#devopsandocker)
25. [Dockerfile and Compose File Reviews](#composefilereviews)
26. [Common Questions and Resources](#extras)

# Introduction

# Setup Docker

# Creating and Using Containers

# Building and Finding Container images

# Persistent Data : Volumes

# Docker Compose

# Swarm Introduction

# Swarm Features

# Swarm Lifecycle

# Container Registries and Image storage and distribution

# Docker in Production

# The kubernetes

# Kubernetes Architecture and Install

# Your first pod

# Inspecting Kubernetes Resources

# exposing Kubernetes Ports

# Kubernetes Management Techinques

# Kubernetes YAML

# Future of Kubernetes

# Automated CI Workflows

# Github Actions

# Docker Secutiy: Defaults and Tools

# Docker 19.03 New Features

# DevOps and Docker

# Dockerfile and Compose File Reviews

# Common Questions, and Resources
