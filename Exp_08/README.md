# EXPERIMENT 08 - CREATING AND EXECUTING YOUR FIRST CONTAINER USING DOCKER

---

## AIM

To create and execute the first **Docker container**.

---

## SOFTWARE REQUIRED

* Docker
* Docker Engine
* Python
* Ubuntu / Linux
* Terminal
* Docker Hub

---

## INTRODUCTION

Docker is a platform used to create and run applications inside **containers**.

In this experiment, a simple Python program is placed inside a Docker image and executed as a Docker container.

---

## PROCEDURE

### 1. Install Docker

For Ubuntu, update the package repository:

```bash
sudo apt update
```

Install Docker:

```bash
sudo apt install docker.io
```

Verify the Docker installation:

```bash
sudo docker run hello-world
```

The lab manual specifies Docker installation and verification using these commands.

---

### 2. Create the Project

Create a new directory for the Docker application.

The project should contain two files:

```text
Docker Project/
│
├── Dockerfile
└── main.py
```

The `main.py` file contains the Python program, while the `Dockerfile` contains the instructions required to create the Docker environment.

---

### 3. Create the Python Program

Create a file named:

```text
main.py
```

Add the following code:

```python
#!/usr/bin/env python3

print("Docker is magic!")
```

When the container executes successfully, the message will be displayed in the terminal.

---

### 4. Create the Dockerfile

Create a file named:

```text
Dockerfile
```

Add:

```dockerfile
FROM python:latest

COPY main.py /

CMD ["python", "./main.py"]
```

The Dockerfile uses the Python image as the base image, copies `main.py` into the image, and defines the command used to execute the Python program.

---

### 5. Build the Docker Image

Open a terminal in the project directory.

Build the image using:

```bash
docker build -t python-test .
```

The `-t` option assigns the name `python-test` to the Docker image.

---

### 6. Run the Docker Container

Run the Docker image:

```bash
docker run python-test
```

The Python application will execute inside the Docker container.

---

## DOCKERFILE

```dockerfile
FROM python:latest

COPY main.py /

CMD ["python", "./main.py"]
```

---

## COMMANDS USED

```bash
sudo apt update

sudo apt install docker.io

sudo docker run hello-world

docker build -t python-test .

docker run python-test
```

---

## USEFUL DOCKER COMMANDS

### List Docker Images

```bash
docker image ls
```

### Remove a Docker Image

```bash
docker image rm [image-name]
```

### List Containers

```bash
docker ps -a
```

### Stop a Container

```bash
docker stop [container-name]
```

### Remove a Container

```bash
docker rm [container-name]
```

### Display Container Logs

```bash
docker logs [container-name]
```

The lab manual provides these commands for managing Docker images and containers.

---

## WORKFLOW

```text
Install Docker
      │
      ▼
Create Project
      │
      ├── main.py
      └── Dockerfile
      │
      ▼
Build Docker Image
      │
      ▼
python-test Image
      │
      ▼
Run Docker Container
      │
      ▼
Execute Python Program
      │
      ▼
Display Output
```

---

## EXPECTED OUTPUT

After running:

```bash
docker run python-test
```

the terminal should display:

```text
Docker is magic!
```

---

## RESULT

Thus, the **first Docker container was successfully created and executed**, and the Python application was successfully run inside the container.

---

