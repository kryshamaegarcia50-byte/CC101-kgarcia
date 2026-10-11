# Docker Compose Guide

## 1. What Does the services: Block Do?

The `services:` block defines the containers that make up the application. In this deployment, there are two services: `database`, which uses the MariaDB 10.6 image, and `app`, which uses the Nextcloud image. Docker Compose manages these services together, making it easier to start, stop, and maintain the application.

## 2. How Does Nextcloud Find the Database Container?

The Nextcloud application uses the environment variable `MYSQL_HOST=database` to locate the database service. The hostname `database` matches the service name defined in the `services:` block. Docker Compose creates a shared network for the services, allowing Nextcloud to communicate with MariaDB using that service name instead of a manually assigned IP address.

Other environment variables configure the database connection:
- `MYSQL_DATABASE=nextcloud_db` specifies the database name.
- `MYSQL_USER=nextcloud_user` specifies the database username.
- `MYSQL_PASSWORD=cloudnova_pass` specifies the database password.
- `MYSQL_ROOT_PASSWORD=cloudnova_root` sets the MariaDB root password.

## 3. Difference Between docker run and docker-compose up -d

The `docker run` command starts an individual container using options supplied in the command. It is useful for running a single service, but managing several connected containers may require multiple commands and manual configuration.

The `docker-compose up -d` command reads the `docker-compose.yml` file and starts all defined services, configures their network, and applies their settings together. The `-d` option runs the containers in the background so the terminal can be used for other tasks.

## Conclusion

Docker Compose makes a multi-container deployment easier to manage because the configuration is stored in one YAML file. In this mission, it connects the Nextcloud application with the MariaDB database and allows both services to be started or stopped together.
