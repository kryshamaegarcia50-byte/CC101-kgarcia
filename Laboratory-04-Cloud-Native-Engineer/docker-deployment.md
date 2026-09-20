
# Docker Deployment

## Checkpoint 3: Verify Docker
```bash
docker --version
docker info
```
Checks if Docker is installed and running.

## Checkpoint 4: Deploy Nginx
```bash
docker pull nginx
docker run -d --name nginx-server -p 8080:80 nginx
docker ps
curl http://localhost:8080
```
Downloads Nginx, runs the container, checks its status, and tests the web server.

## Checkpoint 5: Container Lifecycle
```bash
docker ps
docker stop nginx-server
docker ps -a
docker rm nginx-server
```
Lists, stops, verifies, and removes the Nginx container.

## Summary
I learned how to use Docker to deploy an Nginx web server and manage its container lifecycle.# Docker Deployment
