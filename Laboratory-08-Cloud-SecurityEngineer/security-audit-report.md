# Security Audit Report

## Objective
To inspect the Linux environment and identify basic security information.

## Audit Commands
- `whoami` - Displays the current user.
- `uname -a` - Displays operating system and kernel information.
- `id` - Displays user and group IDs.
- `ss -tuln` - Lists listening network ports.
- `sudo ufw status` - Checks firewall status.

## Findings
These commands help inspect the operating system, current user permissions, listening ports, and firewall status.

## Recommendations
- Use strong passwords.
- Apply system updates regularly.
- Disable unnecessary services.
- Allow only necessary network ports.
- Review user permissions regularly.

## Conclusion
A basic security audit helps identify areas that may need improvement and supports safer system administration.
