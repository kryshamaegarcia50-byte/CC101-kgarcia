# Firewall Configuration

## Objective
Configure UFW to restrict incoming traffic and allow outgoing traffic.

## Commands Used

### 1. Allow SSH
`sudo ufw allow ssh`

This allows incoming SSH connections on the configured SSH port.

### 2. Deny Incoming Traffic by Default
`sudo ufw default deny incoming`

This blocks incoming traffic unless a rule explicitly permits it.

### 3. Allow Outgoing Traffic
`sudo ufw default allow outgoing`

This allows outgoing network connections.

### 4. Enable UFW
`sudo ufw enable`

This activates the firewall.

### 5. Verify Firewall Status
`sudo ufw status verbose`

This displays whether UFW is active, the default policies, and configured rules.

## Expected Security Configuration
- Firewall status: Active
- Default incoming policy: Deny
- Default outgoing policy: Allow
- SSH access: Allowed

Actual results should be confirmed using the terminal output.

## Screenshot
Filename: `firewall-activated.png`

Location: `screenshots/firewall-activated.png`

## Conclusion
UFW helps control network access to the server. Allowing SSH before enabling the firewall helps preserve administrative access, while the default-deny incoming policy reduces exposure to unnecessary connections.

## Checkpoint 5: Granular Port Management

### Objective
Allow legitimate web traffic through TCP port 8080 while keeping the default-deny incoming policy.

### Firewall Rule
Command used:

`sudo ufw allow 8080/tcp`

This rule allows incoming TCP connections on port 8080.

### Verification
Command used:

`sudo ufw status numbered`

The numbered output was used to verify the SSH and TCP port 8080 rules.

### Application Test
Command used:

`curl http://localhost:8080`

A successful response containing the Nginx HTML confirms that the application responds locally. This local test alone does not verify remote firewall access.

### Screenshot
Filename: `firewall-port-allowed.png`

Location: `screenshots/firewall-port-allowed.png`

### Conclusion
Explicitly allowing TCP port 8080 makes the web service accessible through that configured firewall rule while other incoming traffic remains denied by default, unless another rule allows it.
