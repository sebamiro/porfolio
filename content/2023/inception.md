+++
title = "inception"
template = "project.html"
weight = 10
description = "-42 School project"
+++

<a target="blank" href="https://github.com/sebamiro/inception">GitHub</a>

--- 

# Inception

## Summary

Is an individual project about system administration by using dockerfiles
for the creation and management of custom images and micro services.
Use of docker-compose for the deployment of containers, the creation and management of the network and
storage space

```
├── docker-compose.yml
├── requirements
│   ├── mariadb
│   │   ├── Dockerfile
│   │   ├── conf
│   │   │   └── mariadb.conf
│   │   └── tools
│   │       └── mariadb.sh
│   ├── nginx
│   │   ├── Dockerfile
│   │   └── conf
│   │       └── nginx.conf
│   ├── wordpress
│   │   ├── Dockerfile
│   │   ├── conf
│   │   │   └── www.conf
│   │   ├── tools
└   └   └   └── wp.sh
```

## Introduction

This project aims to broaden your knowledge of system administration by using Docker.
You will virtualize several Docker images, creating them in your new personal virtual
machine.

- This project need to be done on a Virtual Machine.
- All the files required for the configuration of your project must be placed in a srcs
folder.
- A Makefile is also required and must be located at the root of your directory. It
must set up your entire application (i.e., it has to build the Docker images using
docker-compose.yml).
- This subject requires putting into practice concepts that, depending on your back-
ground, you may not have learned yet. Therefore, we advise you not to hesitate to
read a lot of documentation related to Docker usage, as well as anything else you
will find helpful in order to complete this assignment.

## Mandatory part

This project consists in having you set up a small infrastructure composed of different
services under specific rules. The whole project has to be done in a virtual machine. You
have to use docker compose.

Each Docker image must have the same name as its corresponding service.
Each service has to run in a dedicated container.
For performance matters, the containers must be built either from the penultimate stable
version of Alpine or Debian. The choice is yours.
You also have to write your own Dockerfiles, one per service. The Dockerfiles must
be called in your docker-compose.yml by your Makefile.
It means you have to build yourself the Docker images of your project. It is then for-
bidden to pull ready-made Docker images, as well as using services such as DockerHub
(Alpine/Debian being excluded from this rule).
You then have to set up:
- A Docker container that contains NGINX with TLSv1.2 or TLSv1.3 only.
- A Docker container that contains WordPress + php-fpm (it must be installed and
configured) only without nginx.
- A Docker container that contains MariaDB only without nginx.
- A volume that contains your WordPress database.
- A second volume that contains your WordPress website files.
- A docker-network that establishes the connection between your containers.

Your containers have to restart in case of a crash.

- In your WordPress database, there must be two users, one of them being the ad-
ministrator. The administrator’s username can’t contain admin/Admin or admin-
istrator/Administrator (e.g., admin, administrator, Administrator, admin-123, and
so forth).

To make things simpler, you have to configure your domain name so it points to your
local IP address.
This domain name must be login.42.fr. Again, you have to use your own login.
For example, if your login is wil, wil.42.fr will redirect to the IP address pointing to
wil’s website.

## Bonus part

For this project, the bonus part is aimed to be simple.

A Dockerfile must be written for each extra service. Thus, each one of them will run
inside its own container and will have, if necessary, its dedicated volume.

Bonus list:
- Set up redis cache for your WordPress website in order to properly manage the
cache.
- Set up a FTP server container pointing to the volume of your WordPress website.
- Create a simple static website in the language of your choice except PHP (Yes, PHP
is excluded!). For example, a showcase site or a site for presenting your resume.
- Set up Adminer.
- Set up a service of your choice that you think is useful. During the defense, you
will have to justify your choice

