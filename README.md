# Welcome to **taller_gittifyca** #
## Content ##
1. Introduction
    * [Overview](#markdown-header-overview) 1. Docker images
    * [Jenkins](#markdown-header-jenkins) 1. Infrastructure
    * [Description](#markdown-header-description)
    * [Diagrams](#markdown-header-diagrams)
## Introduction
### Overview
This project repository has several basic elements for rapid 
test and implementation.
## Docker images
### Jenkins
Here the basic steps to create the image and run the 
container in that image. ```
#!bash
    # Build the image with auto-signed certificate:
    docker build -f jenkins.Dockerfile -t jenkins_img .
    # Start the container in the image previouly build:
    docker run -d -p 8083:8083 --name jenkins -v 
$PWD/jenkins_home:/var/jenkins_home jenkins_img
    # if -v used, the local folder '$PWD/jenkins_home' must 
    # allow permits
    
    # Now the Jenkins can be configured and plugins intalled 
    # For running bash in the jenkins container:
    docker exec -it jenkins bash
    # For stop and remove the jenkins container:
    docker stop jenkins
    docker rm jenkins
    # if -v was used, the local folder '$PWD/jenkins_home' 
    # has all configuration
```
## Infrastructure
### Description Diagrams
