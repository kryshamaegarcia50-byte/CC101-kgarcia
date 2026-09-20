
# Mission Reflection

During this laboratory, I learned how Docker containers work and how they are different from virtual machines. A Docker container has a faster boot and setup process because it shares the host operating system kernel instead of requiring a complete guest operating system. In comparison, a virtual machine needs its own operating system, which requires more time and resources to start.

The port mapping -p 8080:80 is necessary because it connects port 8080 on the host machine to port 80 inside the container. This allows users to access the Nginx web server through http://localhost:8080. Without port mapping, the web server may not be accessible from the host using that port.

When the docker rm command is used, the container is permanently removed. Any data stored only inside the container's writable layer will be lost. However, data stored in persistent volumes can remain available. This taught me that important application data should be stored using appropriate persistent storage.

Containerization helps software developers and IT operations teams work together through DevOps. Developers can package applications with their dependencies, while operations teams can deploy and manage them more consistently. This improves collaboration and reduces deployment problems.

My GitHub portfolio is evolving as I add more laboratory activities and technical documentation. Through this mission, I gained practical experience with Docker commands, container deployment, and lifecycle management. I also learned how to troubleshoot issues, such as KillerCoda session expiration and Git configuration errors. These activities improved my confidence in using cloud technologies and managing my projects.
