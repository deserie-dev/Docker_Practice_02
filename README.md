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
<summary><b>Create Network and Setup MongoDB</b></summary><p>

# commands

## create docker network

```
  docker network create mongo-network
```

## start mongodb

```
  docker run -d -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password --name mongodb --net mongo-network mongo
```

## start mongo-express

```
  docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password --net mongo-network --name mongo-express mongo-express
```

</p></details>

<details>
<summary><b>Docker Compose</b></summary><p>

# Start containers using docker compose

Create docker compose file. (see mongo-docker-compose.yaml)

Run the following command to start all the containers defined in the docker compose file:

```
  docker-compose -f mongo-docker-compose.yaml up
```

To stop the containers run:

```
  docker-compose -f mongo-docker-compose.yaml down
```

</p></details>
