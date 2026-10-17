# Laboratory 08: Cloud Security Engineer

## Mission Overview
This laboratory focuses on securing a Linux web server using security best practices and UFW (Uncomplicated Firewall). An Nginx container is deployed on port 8080, and firewall rules are configured to control incoming and outgoing traffic.

## Objectives
- Understand the Principle of Least Privilege, attack surface, and Default Deny Policy.
- Deploy an Nginx web application using Docker.
- Configure UFW to allow SSH access.
- Set incoming traffic to deny by default and outgoing traffic to allow by default.
- Explicitly allow TCP port 8080.
- Verify firewall rules and test the web application using curl.
- Document the configuration and save screenshots as evidence.

## Commands Executed

### Deploy the Web Application
`docker run -d --name secure-web-app -p 8080:80 nginx`

### Verify the Container
`docker ps`

### Test the Web Application
`curl http://localhost:8080`

### Allow SSH
`sudo ufw allow ssh`

### Set Default Firewall Policies
`sudo ufw default deny incoming`

`sudo ufw default allow outgoing`

### Enable the Firewall
`sudo ufw enable`

### Allow the Web Application Port
`sudo ufw allow 8080/tcp`

### Verify Firewall Rules
`sudo ufw status verbose`

`sudo ufw status numbered`

## Skills Learned
- Basic cloud security principles.
- Linux command-line operations.
- Docker container deployment.
- UFW firewall configuration.
- Managing network ports and access rules.
- Testing web applications with curl.
- Technical documentation and GitHub version control.

## Screenshots
- `screenshots/vulnerable-app-running.png`
- `screenshots/firewall-activated.png`
- `screenshots/firewall-port-allowed.png`
