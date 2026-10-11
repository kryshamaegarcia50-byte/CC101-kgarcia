# Laboratory 06 - Cloud Deployment Engineer

## Mission Overview

This mission focuses on deploying a multi-container application using Docker Compose. The project uses Nextcloud as the web application and MariaDB as the database service. It demonstrates how separate containers work together to provide a private cloud environment.

## Objectives

- Understand the concept of two-tier architecture.
- Identify the roles of the web/application tier and database tier.
- Write a Docker Compose YAML configuration.
- Deploy Nextcloud and MariaDB as separate containers.
- Access the Nextcloud installation page through port 8080.
- Verify the deployment and shut down the containers safely.
- Document the deployment process and save screenshots as evidence.

## Commands Executed

| Command | Purpose |
|---|---|
| `mkdir -p nextcloud-deployment` | Create the project directory. |
| `cd nextcloud-deployment` | Enter the project directory. |
| `nano docker-compose.yml` | Create or edit the Compose configuration. |
| `docker-compose up -d` | Start the services in the background. |
| `docker-compose ps` | Check the container status. |
| `docker-compose logs --tail=50` | View recent container logs. |
| `docker-compose down` | Stop and remove the containers and Compose network. |
| `git add` | Stage changes for Git. |
| `git commit` | Save a version of the changes. |
| `git push origin main` | Upload committed changes to GitHub. |

## Skills Learned

- Understanding multi-tier application architecture.
- Writing and reading Docker Compose YAML files.
- Deploying and managing multiple containers.
- Connecting application and database services through a shared network.
- Checking container status and troubleshooting deployment issues.
- Accessing a web application through a mapped port.
- Documenting technical work and managing project files with GitHub.

## Project Structure

- `README.md` - Mission overview, objectives, commands, and skills learned.
- `multi-tier-architecture.md` - Explanation of the two-tier architecture.
- `docker-compose-guide.md` - Technical explanation of the Compose configuration.
- `reflection.md` - Personal reflection on the mission.
- `screenshots/` - Evidence of deployment, web access, and teardown.
- `docker-compose.yml` - Infrastructure configuration for Nextcloud and MariaDB.

## Deployment Summary

The project defines two services: Nextcloud and MariaDB. Docker Compose manages their configuration and network, while port 8080 exposes the Nextcloud web interface. The deployment was verified using Docker Compose commands and shut down after the required screenshots were captured.
