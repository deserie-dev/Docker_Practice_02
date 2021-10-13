# Docker Practice Project

> Practice Makes Perfect: Another project to practice using Docker

In this challenge set in the DevOps SheCodeAfrica slack channel, I will be following along with [TechWorld with Nana Docker Tutorial](https://youtu.be/3c-iBn73dDE)

**Demo Project**

Stack:

Frontend: HTML. CSS, JS
Backend: Node.js
Database: MongoDB

![](./app/images/5q96wy.gif)

<details>
<summary><b>Pre-Requisites</b></summary><p>
Download and install Docker. I am on a Windows machine running Windows home. I used the following guide to help me: [Windows Subsystem for Linux Installation Guide for Windows 10](https://docs.microsoft.com/en-us/windows/wsl/install-win10). Once I had done that I was able to download [Docker Desktop for Windows](https://docs.docker.com/desktop/windows/install/#system-requirements-for-wsl-2-backend).

</p></details>

<details>
<summary><b>Container vs Image</b></summary><p>

- A container is the running environment for an image.

- You can have multiple containers running on your machine

- An image is made up of different layers

- Images have tags/versions. If you don't specify a version you get the latest version.

- All the artifacts on DockerHub are images.

</p></details>

<details>
<summary><b>Basic Commands</b></summary><p>

**docker pull** pulls image from repo to your machine

**docker ps** list running containers

**docker run** starts a new container from an image

**docker run -d** start container in detached mode, meaning output will be container ID, then container will stop running

**docker stop** stops container

**docker start** starts stopped container

**docker ps -a** lists running and stopped containers

**docker logs** get logs to help debug your container

**docker exec** runs a new command in a running container/ launch a Bash terminal within a container

[OFFICIAL DOCKER COMMANDS CHEATSHEET](https://docs.docker.com/engine/reference/commandline/docker/)

</p></details>

<details>
<summary><b>Debugging Containers</b></summary><p>

</p></details>
