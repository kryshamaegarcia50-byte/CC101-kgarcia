# Laboratory 07: Cloud Operations Engineer

## Mission Overview

The mission of a Cloud Operations Engineer is to monitor the health and performance of a server and its applications. In this laboratory, I established a host system baseline, deployed an Nginx web server using Docker, generated HTTP requests, inspected application logs, and monitored container resource usage. These activities helped me understand how monitoring tools can identify errors and ensure that applications run properly.

## Objectives

- Check the server's RAM usage and available disk storage.
- Establish a baseline of the host system's health.
- Deploy an Nginx web server container named `clientwebsite` using Docker.
- Simulate website visits using `curl`.
- Generate and identify a 404 Not Found error.
- Retrieve and analyze application logs using `docker logs`.
- Monitor container CPU, memory, and network usage using `docker stats`.
- Document monitoring results and save screenshots as evidence.

## Monitoring Commands Executed

| Command | Purpose |
|---|---|
| `free -h` | Checks RAM usage and availability. |
| `df -h /` | Checks the root filesystem's disk capacity and available space. |
| `top` | Displays active processes and CPU usage. |
| `docker run -d --name clientwebsite -p 8080:80 nginx` | Deploys Nginx in a background container and maps port 8080 to port 80. |
| `docker ps` | Lists running containers. |
| `curl http://localhost:8080` | Simulates a successful website visit. |
| `curl http://localhost:8080/hidden-admin-page` | Simulates a request to a nonexistent page to generate a 404 response. |
| `docker logs clientwebsite` | Displays the container's application logs. |
| `docker stats` | Monitors live container CPU, memory, network, and block I/O usage. |

## Skills Learned

- **Host Monitoring:** Learned how to check RAM, disk space, CPU usage, and running processes.
- **Container Deployment:** Practiced deploying an Nginx web server using Docker.
- **Traffic Simulation:** Used `curl` to simulate HTTP requests and generate a 404 error.
- **Log Analysis:** Learned how to inspect application logs and identify successful and failed requests.
- **Resource Monitoring:** Used `docker stats` to measure container CPU and memory consumption.
- **Technical Documentation:** Practiced recording monitoring results and organizing screenshots as evidence.


