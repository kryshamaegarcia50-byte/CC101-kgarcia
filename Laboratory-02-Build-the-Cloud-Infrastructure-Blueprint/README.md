## Mission Overview
Congratulations, your onboarding has been successfully completed, and 
your Cloud Computing Portfolio has been approved by your supervisor.

CloudNova Technologies has now assigned you to your first official 
project. Before deploying cloud services, every cloud engineer must 
understand the infrastructure that powers modern cloud computing. This 
mission was to investigate the components of cloud infrastructure, 
identify how compute, storage, networking, and identity services work 
together, and document the findings as if preparing technical 
documentation for a client.

Using the KillerCoda Playground, Linux tools, official cloud 
documentation, and the GitHub Cloud Computing Portfolio, a series of 
engineering tasks were completed to simulate the planning phase of a 
cloud deployment.

*"Great cloud engineers build systems—but exceptional cloud engineers 
document and justify every design decision."*

## Objectives
At the end of this laboratory activity, the goal was to be able to:
- Explain the major components of cloud infrastructure.
  
- Investigate the hardware and software resources available in a Linux 
  environment.
  
- Differentiate compute, storage, networking, and identity resources.
  
- Interpret the relationship between cloud infrastructure components.
  
- Create professional technical documentation using Markdown.
  
- Continue building a structured GitHub Cloud Computing Portfolio.

## Cloud Infrastructure Components
Five main components were investigated on the KillerCoda Linux server:

| Component | What Was Found |
|---|---|
| **Operating System** | Ubuntu 24.04.4 LTS (Noble Numbat), kernel 6.8.0-138-generic |
| **Compute** | 1 CPU core, Intel Xeon E312xx (Sandy Bridge, IBRS update) — a virtualized CPU |
| **Memory** | 1.9 GiB total Memory,with approximately 1.5 GiB available; 1.0 GiB swap space|
| **Storage** | 20G virtual disk (`vda`); root partition (`/dev/vda1`) has 19G total, 5.4G used, and 13G available |
| **Networking** | Hostname: `ubuntu`; primary interface: `enp1s0 `with IP `172.30.1.2`; Docker bridge: `docker0` with IP `172.17.0.1` |

## Tools Used
- **KillerCoda Playground** — provided the live Linux server environment
- **Linux terminal** — used to run investigation commands
- **Draw.io (diagrams.net)** — used to create the cloud architecture diagram
- **GitHub** — used to build and maintain the Cloud Computing Portfolio
- **Markdown** — used for all technical documentation

 ## Linux Commands Executed
| Purpose | Command |
|---|---|
| Operating System | `cat /etc/os-release` |
| Kernel Version | `uname -r` |
| CPU Model | `cat /proc/cpuinfo \| grep "model name"` |
| Number of CPU Cores | `nproc` |
| Total RAM | `free -h` |
| Disk Capacity | `df -h` |
| Mounted File Systems | `mount \| column -t` |
| Hostname | `hostname` |
| IP Address | `hostname -I` |

## Skills Learned
-Create and configure cloud infrastructure.

-Connect to and manage a Linux environment.

-Execute Linux commands through the terminal.

-Install and configure required software.

-Verify whether services are running correctly.

-Use GitHub to store and document project work.

-Write technical documentation using Markdown.

## Challenges Encountered
Some challenges encountered during the project included:

-Configuring the cloud infrastructure correctly.

-Understanding and executing Linux commands.

-Troubleshooting configuration or connection problems.

-Making sure the required services were running correctly.

-Verifying that the final setup worked as expected.
