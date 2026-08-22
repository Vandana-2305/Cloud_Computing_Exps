# Cloud_Computing_Exps
# ☁️ Cloud Computing Lab

> **Course Code:** CS4V51
> **Course:** Cloud Computing Lab
> **Practical Exercises:** 9
> **Repository:** Cloud Computing Laboratory Experiments

---

## 📌 About

This repository contains the practical experiments performed as part of the **Cloud Computing Lab**.

The experiments cover fundamental concepts and hands-on implementation of:

* Virtual Machines and Virtual Workstations
* C Compiler installation in Virtual Machines
* Google App Engine (GAE)
* Cloud application deployment
* CloudSim simulation
* File transfer between Virtual Machines
* Hadoop Single Node Cluster
* Docker Containers
* Docker Hub

---

## 🧪 List of Experiments

| No.    | Experiment                      | Description                                                                 |
| ------ | ------------------------------- | --------------------------------------------------------------------------- |
| **01** | 🖥️ Virtual Workstation         | Install VirtualBox/VMware and create a Guest OS                             |
| **02** | 💻 Virtual Machine – C Compiler | Install a C compiler in a Virtual Machine and execute simple programs       |
| **03** | 🌐 Google App Engine            | Install GAE and create a Hello World web application                        |
| **04** | 🚀 GAE Launcher                 | Use GAE tools to launch web applications                                    |
| **05** | ☁️ CloudSim                     | Simulate a cloud scenario using CloudSim                                    |
| **06** | 📂 VM File Transfer             | Transfer files between Virtual Machines                                     |
| **07** | 🐘 Hadoop                       | Install a Hadoop Single Node Cluster and run applications such as WordCount |
| **08** | 🐳 Docker Container             | Create and execute the first Docker container                               |
| **09** | 📦 Docker Hub                   | Run a container using an image from Docker Hub                              |

The experiment list and titles are taken from the laboratory manual.

---

## 📁 Repository Structure

```text
Cloud-Computing-Lab/
│
├── README.md
│
├── Exp_01/
│   └── README.md
│
├── Exp_02/
│   └── README.md
│
├── Exp_03/
│   └── README.md
│
├── Exp_04/
│   └── README.md
│
├── Exp_05/
│   └── README.md
│
├── Exp_06/
│   └── README.md
│
├── Exp_07/
│   └── README.md
│
├── Exp_08/
│   └── README.md
│
└── Exp_09/
    └── README.md
```

---

## 🛠️ Technologies & Tools

The experiments use a range of cloud-computing and virtualization technologies:

### Virtualization

* Oracle VM VirtualBox
* VMware Workstation / Player
* Guest Operating Systems

### Cloud Platforms

* Google App Engine
* Google Cloud SDK

### Cloud Simulation

* CloudSim
* Eclipse IDE
* Apache Commons Math

### Big Data

* Apache Hadoop
* HDFS
* YARN
* MapReduce

### Containerization

* Docker
* Docker Hub
* Docker Images
* Docker Containers

---

## 🎯 Learning Objectives

By completing these experiments, the following concepts are explored:

1. Understand the fundamentals of **virtualization**.
2. Create and configure **Virtual Machines**.
3. Install and execute software inside a Guest OS.
4. Understand the basics of **Platform as a Service (PaaS)** using Google App Engine.
5. Create and deploy simple cloud applications.
6. Simulate cloud environments using **CloudSim**.
7. Understand file sharing and transfer between virtual machines.
8. Configure a **Hadoop Single Node Cluster**.
9. Understand **HDFS, YARN and MapReduce**.
10. Create and execute applications using **Docker containers**.
11. Pull and run container images from **Docker Hub**.

---

## 📚 Experiment Overview

### Experiment 01 - Virtual Workstation

Installation and configuration of VirtualBox/VMware with a Guest Operating System.

**Main Topics:**

* Virtualization
* VirtualBox
* Host OS
* Guest OS
* Virtual Machine configuration

---

### Experiment 02 - Virtual Machine – C Compiler

Installation of a C compiler inside a Virtual Machine and execution of simple C programs.

**Main Topics:**

* Virtual Machine
* C Compiler
* GCC
* C Program Compilation
* Program Execution

---

### Experiment 03 - Google App Engine

Installation of Google App Engine and creation of a simple **Hello World** web application.

**Main Topics:**

* Google App Engine
* Web Applications
* Python / Java
* Application Deployment

---

### Experiment 04 - GAE Launcher

Use Google App Engine tools to create, configure and launch web applications. The manual covers project configuration, `app.yaml`, application files and deployment using `gcloud app deploy`.

**Main Topics:**

* Google Cloud SDK
* App Engine
* `app.yaml`
* Static Web Application
* Application Deployment

---

### Experiment 05 - CloudSim

Simulation of a cloud scenario using **CloudSim** and execution of cloud-related scheduling experiments.

**Main Topics:**

* Cloud Simulation
* CloudSim
* Eclipse
* Java
* Scheduling Algorithms

---

### Experiment 06 - File Transfer Between Virtual Machines

Study and implementation of different methods for transferring files between virtual machines.

The manual discusses:

* Copy and Paste
* USB Drive
* Network Share
* VirtualBox Drag and Drop
* Shared Folders

---

### Experiment 07 - Hadoop Single Node Cluster

Installation and configuration of a **Hadoop Single Node Cluster** and execution of simple applications such as WordCount.

The manual introduces the major Hadoop components:

* Hadoop Common
* HDFS
* YARN
* MapReduce

---

### Experiment 08 - First Docker Container

Creation and execution of the first Docker container.

The experiment uses a simple Python application with:

```text
Dockerfile
main.py
```

The Docker image is built and executed using Docker commands.

---

### Experiment 09 - Docker Hub

Running containers using images available from **Docker Hub**.

## The experiment demonstrates working with Docker containers and Docker Hub images, including running an Nginx container.

## 📊 Skills Covered

```text
Virtualization
     │
     ├── VirtualBox / VMware
     │
     ▼
Virtual Machines
     │
     ├── Guest Operating Systems
     ├── Software Installation
     └── File Transfer
     │
     ▼
Cloud Platforms
     │
     ├── Google App Engine
     └── Cloud Deployment
     │
     ▼
Cloud Simulation
     │
     └── CloudSim
     │
     ▼
Big Data
     │
     └── Hadoop
          ├── HDFS
          ├── YARN
          └── MapReduce
     │
     ▼
Containerization
     │
     ├── Docker
     ├── Docker Images
     ├── Docker Containers
     └── Docker Hub
```

---

## 📂 Experiment-wise Documentation

Each experiment has its own directory containing a dedicated `README.md` file.

```text
Exp_01 → Virtual Workstation
Exp_02 → Virtual Machine – C Compiler
Exp_03 → Google App Engine
Exp_04 → GAE Launcher
Exp_05 → CloudSim
Exp_06 → VM File Transfer
Exp_07 → Hadoop Single Node Cluster
Exp_08 → First Docker Container
Exp_09 → Docker Hub
```

Each individual README contains:

* 🎯 Aim
* 🛠️ Requirements
* 📋 Procedure
* 💻 Commands / Configuration
* 📸 Expected Output
* ✅ Result
* 📚 Experiment Summary

---

## 🚀 How to Use This Repository

1. Clone the repository.

```bash
git clone <repository-url>
```

2. Open the project directory.

```bash
cd Cloud-Computing-Lab
```

3. Navigate to the required experiment.

```bash
cd Exp_01
```

4. Open the corresponding `README.md`.

5. Follow the experiment procedure step by step.

---


### ☁️ Cloud Computing Lab

**9 Experiments • Virtualization • Cloud Platforms • Simulation • Big Data • Containers**

---
