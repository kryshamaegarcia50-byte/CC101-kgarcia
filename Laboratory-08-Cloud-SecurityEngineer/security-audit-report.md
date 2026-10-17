# Security Audit Report

## Checkpoint 2: Research — Security Best Practices

### 1. Principle of Least Privilege (PoLP)

The Principle of Least Privilege means giving users and applications only the permissions they need to perform their assigned tasks. It is important for cloud accounts because it reduces the risk of unauthorized access, accidental changes, and damage if an account is compromised. For example, a user who only needs to view files should not automatically receive permission to delete them or manage the entire cloud environment.

### 2. Attack Surface

The attack surface is the collection of entry points that an attacker could potentially use to access or compromise a virtual machine. These may include open network ports, running services, applications, user accounts, and outdated software. Reducing unnecessary services, closing unused ports, and applying security updates can help make the virtual machine more secure.

### 3. Default Deny Policy

A Default Deny Policy means blocking network traffic unless a specific rule allows it. This is safer than trying to block individual hackers because new or unknown threats may appear from many different addresses. By allowing only the connections that are necessary, administrators can reduce unauthorized access and limit the services exposed to potential attackers.

## Conclusion

These three security practices help protect cloud infrastructure. Least privilege limits permissions, reducing the attack surface removes unnecessary entry points, and default deny restricts network traffic to explicitly approved connections. Applying these practices can reduce security risks and help maintain a safer cloud environment.
