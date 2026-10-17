# Mission Reflection

Throughout this laboratory, I learned that monitoring is an important part of being a Cloud Operations Engineer. I realized that even if containers are running perfectly, checking the host server's resources is still necessary. The server may run out of memory or disk space, which can cause applications to slow down, crash, or become unavailable. Monitoring the host helps prevent these problems before they affect users.

If a user complains that they cannot log into a web application, I would use the `docker logs` command to check the container's application logs. These logs may show error messages, failed requests, or other problems that can help me identify the cause. For example, I might find an authentication error or a connection problem between the application and its database. This information would help me investigate the issue instead of guessing.

I also learned the difference between logs and metrics. Logs provide detailed records of events, such as successful HTTP requests and 404 errors. Metrics show numerical information about performance, such as CPU usage, memory consumption, and network activity. Both are important because logs explain what happened, while metrics help show how well a system is performing.

Large enterprise companies may use monitoring tools such as Prometheus and Grafana to manage thousands of containers. Prometheus collects and stores metrics from different systems, while Grafana displays the information through dashboards and graphs. These tools help engineers monitor many containers, detect unusual activity, and respond to problems more quickly.

Finally, this laboratory improved my ability to troubleshoot Linux environments. I practiced checking memory and disk space, deploying an Nginx container, generating HTTP requests, reading application logs, and monitoring container resources. I became more familiar with Docker commands and learned how to use actual terminal output to identify potential problems. Overall, this experience helped me understand how monitoring and troubleshooting support reliable and stable cloud applications.
