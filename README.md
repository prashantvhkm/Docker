# 🐳 Docker Learning Repository

Welcome to my **Docker Learning Repository**.

This repository contains my practical Docker learning notes, commands, examples, and exercises. The goal is to learn Docker step by step, starting from basic container commands and gradually moving toward real-world application deployment.

---

## 📚 Repository Structure

```text
Docker/
│
├── Day01/
│   └── Day01.md
│
└── README.md
```

### Day01

The `Day01` folder contains the first set of Docker learning notes.

Topics covered:

- Docker version
- Docker images
- Docker containers
- Running containers
- Starting and stopping containers
- Executing commands inside containers
- Opening Bash inside containers
- Port mapping
- Environment variables
- Docker networks
- Bridge network
- Host network
- None network
- Custom Docker networks
- Container-to-container communication
- Docker command cheat sheet

---

## 🎯 Learning Goals

The main purpose of this repository is to build practical knowledge of Docker.

The learning path will progress through:

```text
Docker Basics
     ↓
Containers
     ↓
Images
     ↓
Dockerfile
     ↓
Docker Build
     ↓
Docker Volumes
     ↓
Docker Networks
     ↓
Docker Compose
     ↓
Docker Hub
     ↓
.NET API with Docker
     ↓
React with Docker
     ↓
SQL Server + Docker
     ↓
Redis + Docker
     ↓
Full Stack Application
     ↓
Docker Deployment
     ↓
Kubernetes
```

---

## 🐳 What is Docker?

Docker is a platform used to package and run applications in isolated environments called **containers**.

A Docker container contains the application and the dependencies required to run it.

Basic concept:

```text
Application
     │
     ├── Dependencies
     ├── Configuration
     └── Runtime
            │
            ↓
       Docker Image
            │
            │ docker run
            ↓
       Docker Container
```

---

## 🧱 Image vs Container

### Docker Image

An image is a template used to create containers.

Examples:

```text
ubuntu
nginx
redis
mysql
mssql
```

### Docker Container

A container is a running or created instance of a Docker image.

```text
Docker Image
     │
     │ docker run
     ↓
Docker Container
```

---

## 🔧 Basic Commands

Check Docker version:

```bash
docker -v
```

Run an Ubuntu container:

```bash
docker run -it ubuntu
```

Show running containers:

```bash
docker ps
```

Show all containers:

```bash
docker ps -a
```

Show Docker images:

```bash
docker images
```

Start a container:

```bash
docker start <container>
```

Stop a container:

```bash
docker stop <container>
```

Open a Bash shell:

```bash
docker exec -it <container> bash
```

View container logs:

```bash
docker logs <container>
```

---

## 🌐 Port Mapping

Docker can map a host machine port to a container port.

Syntax:

```bash
docker run -p HOST_PORT:CONTAINER_PORT IMAGE
```

Example:

```bash
docker run -it -p 1025:80 ubuntu
```

Concept:

```text
Host Machine
    │
    │ Port 1025
    ↓
Docker Container
    │
    │ Port 80
    ↓
Application
```

---

## ⚙️ Environment Variables

Environment variables can be passed to containers using `-e`.

Example:

```bash
docker run -it -e APP_ENV=Development -e APP_NAME=MyApp ubuntu
```

Multiple variables can be passed to the same container.

---

## 🌐 Docker Networks

List networks:

```bash
docker network ls
```

Inspect a network:

```bash
docker network inspect bridge
```

Create a custom network:

```bash
docker network create -d bridge homenetwork
```

Run a container on the custom network:

```bash
docker run -it --network=homenetwork --name=test01 ubuntu
```

Docker networks allow containers to communicate with each other.

Example:

```text
        homenetwork
             │
      ┌──────┴──────┐
      ↓             ↓
   test01         test02
```

---

## 📖 Day 01

Day 01 focuses on Docker fundamentals and command-line usage.

The complete notes are available here:

[`Day01/DOCKER_NOTES.md`](Day01/DOCKER_NOTES.md)

---

## 🚀 Future Learning

Future folders will contain practical examples such as:

```text
Day01  → Docker Basics
Day02  → Dockerfile
Day03  → Docker Images & Build
Day04  → Docker Volumes
Day05  → Docker Networks
Day06  → Docker Compose
Day07  → Docker Hub
Day08  → .NET API + Docker
Day09  → React + Docker
Day10  → SQL Server + Docker
Day11  → Redis + Docker
Day12  → Full Stack Docker Project
Day13  → Docker Deployment
Day14  → Kubernetes Basics
```

---

## 💻 Technology Stack

This repository will focus mainly on:

- Docker
- Docker CLI
- Dockerfile
- Docker Compose
- ASP.NET Core / .NET
- React
- SQL Server
- Redis
- Linux
- Kubernetes

---

## 👨‍💻 Learning Approach

The repository follows a practical approach:

```text
Learn
  ↓
Write Command
  ↓
Run Command
  ↓
Understand Output
  ↓
Build Example
  ↓
Document
  ↓
Repeat
```

The objective is not only to memorize Docker commands, but to understand how containers, images, networks, volumes, and application deployments work together.

---

## ⭐ Repository Status

🚧 **Currently learning Docker**

Current progress:

- [x] Docker installation / version check
- [x] Run containers
- [x] List containers
- [x] Start / stop containers
- [x] Execute commands
- [x] Docker images
- [x] Port mapping
- [x] Environment variables
- [x] Docker networks
- [x] Custom networks
- [ ] Dockerfile
- [ ] Docker build
- [ ] Docker volumes
- [ ] Docker Compose
- [ ] Docker Hub
- [ ] .NET + Docker
- [ ] React + Docker
- [ ] SQL Server + Docker
- [ ] Redis + Docker
- [ ] Kubernetes

---

## 📌 Notes

This is a personal learning repository created to practice Docker concepts through hands-on examples.

More topics and practical projects will be added as the learning progresses.

---

# 🐳 Keep Learning Docker
