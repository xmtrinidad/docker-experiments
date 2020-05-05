# Docker Docs and Udemy Tutorial

Experimenting with Docker using the following resources:

https://www.udemy.com/course/docker-mastery/
https://docs.docker.com/

# Basic commands

Docker commands are usually in the following format:

```docker <command> (options)``` (old docker)

```docker <command> <sub-command> (options)``` (new docker)

* docker version
* docker info

## Image vs Container

* An **Image** is the application we want to run
* A **Container** is an instance of that image running as a process
* You can have many containers running off the same image
* Docker's default image "registry" is called Docker Hub

## nginx Example

```docker container run --publish 80:80 --detach nginx```

**--detach** runs the container in the background

## One Liner to stop and remove all containers

```docker stop $(docker ps -a -q)```
```docker rm $(docker ps -a -q)```

 from https://coderwall.com/p/ewk0mq/stop-remove-all-docker-containers

## Section 3 Commands Continued

`docker container inspect <containerid>`
`docker container stats`

## Getting a A Shell Inside Containers

`docker container run -it --name proxy nginx bash`
