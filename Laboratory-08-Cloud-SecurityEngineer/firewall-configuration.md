# Firewall Configuration

## Objective
To understand how a Linux firewall protects a system by controlling network traffic.

## Firewall Tool
UFW (Uncomplicated Firewall) is a Linux tool used to manage firewall rules.

## Commands Used
- `sudo ufw status` - Checks whether UFW is active.
- `sudo ufw status verbose` - Displays detailed firewall status.
- `sudo ufw app list` - Lists available application profiles.

## Security Best Practices
- Allow only necessary network ports.
- Restrict SSH access to trusted users and networks.
- Review firewall rules regularly.
- Avoid exposing unnecessary services.
- Verify access requirements before changing firewall settings.

## Conclusion
Firewall rules help protect systems against unauthorized network access. Rules should be reviewed carefully before they are applied.
