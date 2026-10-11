# Mission Reflection

In this mission, I learned how Docker Compose makes cloud deployment easier and more organized. Instead of manually typing separate commands to create and configure each container, I can write everything in one `docker-compose.yml` file. This file defines the services, images, environment variables, ports, and connections needed by the application. With the `docker-compose up -d` command, I can start the services together, saving time and reducing repetitive work.

I also learned that YAML indentation is very important. YAML uses spaces to show the relationship between configuration settings. If I use a Tab instead of spaces or place a line at the wrong indentation level, the configuration may fail to load or may not work as expected. This taught me to be careful when writing configuration files and to check my code before deploying.

Environment variables, such as `MYSQL_PASSWORD` and `MYSQL_DATABASE`, provide the settings that the application and database need to communicate. They make configuration easier to manage because values can be defined separately from the application's code. However, I also learned that passwords written directly in a Compose file are not ideal for production. More secure methods, such as environment files with proper access controls or secret management tools, should be used for sensitive information.

Deploying Nextcloud with MariaDB in just a few minutes felt exciting and rewarding. Seeing the Nextcloud installation page in the browser helped me understand how different containers work together to provide a cloud service. Checking the containers and shutting them down properly also gave me practical experience in managing infrastructure.

Since Mission 1, my understanding of cloud computing has improved. At first, I mainly understood cloud computing as using online services and remote servers. Now, I have a better understanding of how infrastructure, containers, networking, storage, and automation work together. This mission helped me realize that cloud engineers need both technical skills and careful documentation to build and manage reliable systems.
