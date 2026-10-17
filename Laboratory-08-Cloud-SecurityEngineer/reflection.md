# Mission Reflection

Completing this Cloud Security Engineer mission helped me understand why protecting a server is an important responsibility in cloud computing. I learned that security is not only about protecting the physical network but also about securing the server itself.

A host-based firewall protects a server by controlling incoming and outgoing network traffic directly on the machine. Even if an attacker breaches the network perimeter, the firewall can still block unauthorized connections based on its configured rules. This provides an additional layer of protection against potential attacks.

Managing open network ports is also important because every unnecessary open port can become a possible entry point for attackers. By allowing only the ports required by the application, administrators can reduce the server's attack surface. In this mission, I allowed SSH for administration and TCP port 8080 for the Nginx web application while keeping the default incoming policy set to deny.

In a real enterprise environment, leaving a database port such as 3306 for MySQL open to the public internet is dangerous because attackers may attempt password guessing, exploit vulnerabilities, or access sensitive information if the database is not properly secured. Database access should normally be restricted to trusted application servers and authorized administrators.

This mission changed my perspective on how easily a server can be exposed to security threats. Before this activity, I did not fully appreciate how a single open port or an incorrect firewall rule could create a security risk. I learned that small configuration decisions can make a significant difference in protecting systems.

My GitHub portfolio now provides a place to organize and demonstrate the knowledge and practical skills I have gained through my eight cloud engineering missions. It contains documentation, command examples, research, and screenshots of completed activities. This portfolio can help me track my progress, review what I have learned, and demonstrate my growing technical abilities. Overall, this mission taught me that cybersecurity requires careful configuration, regular monitoring, and continuous improvement.
