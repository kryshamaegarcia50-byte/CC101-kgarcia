# Firewall Configuration

## Checkpoint 4: Building the Firewall

### 1. Allow SSH
Command:
`sudo ufw allow ssh`

This rule allows incoming SSH connections so administrators can manage the server remotely.

### 2. Set the Default Deny Policy
Command:
`sudo ufw default deny incoming`

This blocks incoming connections unless an explicit rule allows them.

### 3. Allow Outgoing Traffic
Command:
`sudo ufw default allow outgoing`

This permits outgoing connections initiated by the server.

### 4. Enable the Firewall
Command:
`sudo ufw enable`

This activates UFW and applies the configured firewall policies.

### 5. Verify Firewall Status
Command:
`sudo ufw status verbose`

This displays the firewall status, default policies, and configured rules.

## Checkpoint 5: Granular Port Management

### 6. Allow TCP Port 8080
Command:
`sudo ufw allow 8080/tcp`

This allows incoming TCP traffic on port 8080 for the web application.

### 7. Verify Numbered Rules
Command:
`sudo ufw status numbered`

This displays the configured firewall rules with their numbers.

### 8. Test the Web Application
Command:
`curl http://localhost:8080`

This sends a local HTTP request to the Nginx web server and displays its response.

## SSH Safety Explanation

If `sudo ufw enable` is run before `sudo ufw allow ssh`, the firewall may block incoming SSH connections and lock administrators out of the server.

## Final Firewall Configuration

- Firewall status: Active
- Default incoming policy: Deny
- Default outgoing policy: Allow
- SSH: Explicitly allowed
- TCP port 8080: Explicitly allowed

Actual status and rules should be confirmed using the terminal output.

## Screenshots

- `screenshots/firewall-activated.png`
- `screenshots/firewall-port-allowed.png`

## Conclusion

UFW provides a simple way to control network access. Allowing SSH before enabling the firewall helps preserve remote administration, while the default-deny policy and explicit port rules reduce unnecessary exposure.
