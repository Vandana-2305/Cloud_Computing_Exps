# EXPERIMENT 09: Run a Container from Docker Hub

---

## Aim

To write a program to run a container from Docker Hub.

---

## Objective

* To understand Docker Hub and container images.
* To pull an image from Docker Hub.
* To create and run a Docker container using the Docker CLI.
* To understand basic Docker container management commands.

---

## Software Requirements

* Docker
* Docker CLI
* Docker Hub
* Ubuntu Docker Image
* Linux / Windows / macOS system with Docker installed

---

## Experiment Description

Docker allows applications to be packaged and executed inside lightweight containers. Docker Hub provides publicly available container images that can be downloaded and used to create containers.

In this experiment, the `ubuntu` image available on Docker Hub is used to create and run a container. If the image is not available locally, Docker automatically pulls it from Docker Hub before starting the container.

---

## Procedure

### Step 1: Verify Docker Installation

Open the terminal and display the Docker command-line help:

```bash
docker -h
```

The command displays the available Docker commands and management options.

---

### Step 2: Run the First Container

Run the following command:

```bash
docker container run -it ubuntu top
```

Here:

* `docker container run` creates and starts a container.
* `-i` keeps the standard input open.
* `-t` allocates a pseudo-terminal.
* `ubuntu` is the Docker image obtained from Docker Hub.
* `top` is the command executed inside the container.

If the Ubuntu image is not available locally, Docker pulls the `ubuntu:latest` image from Docker Hub automatically.

---

## Useful Docker Commands

### List Containers

```bash
docker container ls
```

Displays currently running containers.

### List All Containers

```bash
docker ps -a
```

Displays running and stopped containers.

### Stop a Container

```bash
docker stop [container_name]
```

### Remove a Container

```bash
docker rm [container_name]
```

### Display Container Logs

```bash
docker logs [container_name]
```

### List Docker Images

```bash
docker image ls
```

### Remove a Docker Image

```bash
docker image rm [image_name]
```

The above commands are listed in the lab manual for basic Docker image and container management.

---

## Expected Output

When the command is executed, Docker downloads the Ubuntu image if it is not already present and starts the container.

Example:

```text
Unable to find image 'ubuntu:latest' locally
latest: Pulling from library/ubuntu
Pull complete
Pull complete
Pull complete
Digest: sha256:...
Status: Downloaded newer image for ubuntu:latest
```

The Ubuntu container then starts and executes the `top` command.

---

## Result

Thus, the program to run a container from Docker Hub was executed and verified successfully.

---

## Conclusion

The experiment demonstrates how to obtain a Docker image from Docker Hub and use it to create and execute a container using Docker CLI commands.

---

## Key Commands

```bash
docker -h
docker container run -it ubuntu top
docker container ls
docker ps -a
docker stop [container_name]
docker rm [container_name]
docker image ls
docker image rm [image_name]
docker logs [container_name]
```

