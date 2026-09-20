
# Laboratory 04 - Cloud Native Engineer

## Mission Overview

This laboratory focuses on cloud-native technologies, virtualization, containers, and Docker deployment. We learned how to run and manage containers using Docker.

## Objectives

- Understand the differences between virtual machines and containers.
- Learn basic Docker commands.
- Deploy an Nginx web server using Docker.
- Practice managing the container lifecycle.

## Docker Commands Executed

### Checkpoint 3: Docker Playground

```bash
docker --version
docker info
```

### Checkpoint 4: Deploy Nginx Container

```bash
docker pull nginx
docker run -d --name nginx-server -p 8080:80 nginx
docker ps
curl http://localhost:8080
```

### Checkpoint 5: Container Lifecycle

```bash
docker ps
docker stop nginx-server
docker ps -a
docker rm nginx-server
```

## Skills Learned

- Basic Docker installation verification.
- Pulling images from Docker Hub.
- Running containers in detached mode.
- Mapping ports between the host and container.
- Managing and removing Docker containers.
- Using terminal commands in a cloud environment.

## Challenges Encountered

One challenge I encountered was the KillerCoda playground reconnecting and expiring after one hour. I solved this by reconnecting and cloning my GitHub repository again. I also learned how to check Docker commands and manage containers using the terminal.# Laboratory 04 - Cloud Native Engineer
