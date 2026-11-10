# Networkwalks B084 — Cybersecurity Week 1 Lab Setup

A hands-on cybersecurity lab project focused on building a secure virtual environment using Oracle VirtualBox and Kali Linux. This repository documents the setup process, configuration steps, and validation checks needed to create a practical learning lab for networking, Linux administration, and ethical hacking fundamentals.

## Overview

This project was created to help students understand how to configure a cybersecurity lab in a safe, isolated environment. By using a virtual machine instead of a physical system, learners can explore cybersecurity tools, test basic commands, and practice networking concepts without risking the host system or production environments.

This repository is especially suitable for beginner cybersecurity students, IT learners, and anyone interested in hands-on security practice in a controlled lab environment.

---

## Project Status

Status: Completed

This lab setup demonstrates the installation and configuration of a virtual cybersecurity environment with the following goals:

- Set up a local virtual lab environment
- Install and configure Kali Linux
- Use Oracle VirtualBox to host the machine
- Validate connectivity and resource allocation
- Document the workflow for future experiments

---

## Why This Repository Is a Strong Student Project

This project is a strong student repository because it combines academic learning, practical setup, and real-world tools. It showcases:

- Virtualization fundamentals
- Linux system configuration
- Network troubleshooting and verification
- Safe experimentation in an isolated environment
- Clear documentation and a structured learning path
- A foundation for future cybersecurity and SOC-related labs

---

## Learning Objectives

By completing this lab, students will be able to:

- Install Oracle VirtualBox on a host machine
- Deploy Kali Linux as a virtual machine
- Configure VM hardware and networking resources
- Understand virtual network modes and their uses
- Verify IP addressing, routing, and DNS resolution
- Run security and network tools in a controlled environment
- Create a snapshot for system recovery and safe testing

---

## Lab Architecture

```text
+--------------------------------------+
|          Host Machine                |
|       Windows 10 / 11 / older OS     |
+--------------------------------------+
                    |
                    v
+--------------------------------------+
|           Hypervisor                 |
|       Oracle VirtualBox             |
+--------------------------------------+
                    |
                    v
+--------------------------------------+
|        Virtual Machine              |
|          Kali Linux                 |
+--------------------------------------+
                    |
                    v
+--------------------------------------+
|       Cybersecurity Lab             |
|  Ethical Hacking & Security Tools  |
+--------------------------------------+
```

### Lab Components

| Component | Description |
|---|---|
| Host Operating System | Machine used to run the virtual environment |
| Hypervisor | Oracle VirtualBox |
| Guest Operating System | Kali Linux |
| Purpose | Cybersecurity learning and ethical testing |
| Network Environment | Isolated virtual network |
| Tools | Nmap, Wireshark, Metasploit, Linux utilities |
| Security Model | Safe and controlled environment |

---

## Technologies and Tools

| Tool | Purpose |
|---|---|
| Kali Linux | Penetration testing and security analysis |
| Oracle VirtualBox | Virtual machine creation and management |
| Nmap | Network discovery and port scanning |
| Wireshark | Network traffic analysis |
| Metasploit Framework | Security testing and exploitation practice |
| Linux Commands | Networking, system checks, and troubleshooting |

---

## Prerequisites

Before beginning the lab, make sure you have:

- A computer with sufficient hardware resources
- Oracle VirtualBox installed
- A Kali Linux ISO or virtual appliance image
- Enough RAM and storage for the guest machine
- Internet access to download files and tools
- Administrative privileges on the host machine

---

## Step-by-Step Setup Guide

### Step 1: Install Oracle VirtualBox

Download and install Oracle VirtualBox from the official site:

- Oracle VirtualBox Downloads: https://www.virtualbox.org/wiki/Downloads

### Step 2: Download Kali Linux

Download the official Kali Linux ISO or a VirtualBox-ready image from the official project website:

- Kali Linux Downloads: https://www.kali.org/get-kali/

### Step 3: Extract the Archive

If the Kali Linux image is compressed, extract it using a tool such as 7-Zip before importing it into VirtualBox.

- 7-Zip: https://www.7-zip.org/

### Step 4: Import Kali Linux into VirtualBox

1. Open Oracle VirtualBox.
2. Select File → Import Appliance if using an OVA file.
3. Alternatively, create a new VM and attach the Kali Linux ISO.
4. Review the VM configuration.
5. Start the Kali Linux virtual machine.

### Step 5: Configure Virtual Machine Resources

Allocate resources according to the performance of your host machine.

| Resource | Recommended Configuration |
|---|---|
| Memory (RAM) | Based on host capacity; usually 2–8 GB |
| CPU Cores | Based on available host CPU resources |
| Virtual Disk | Kali Linux virtual disk |
| Network Adapter | VirtualBox network mode |
| Graphics Memory | Adjust as needed for performance |

### Step 6: Configure Network Connectivity

Choose the networking mode that best fits your lab requirements.

- NAT: Provides internet access through the host
- NAT Network: Enables communication between multiple VMs and outbound access
- Host-Only Adapter: Connects the host and guest systems directly
- Internal Network: Creates an isolated network between virtual machines

For security learning, an isolated or dedicated lab network is recommended.

### Step 7: Verify Kali Linux Functionality

Open the terminal in Kali Linux and run the following commands:

```bash
# Display network interfaces and IP addresses
ip a

# Display routing information
ip route

# Check internet connectivity
ping -c 4 8.8.8.8

# Verify DNS resolution
nslookup google.com

# Check Nmap installation
nmap --version

# Display operating system information
cat /etc/os-release
```

### Step 8: Create a Recovery Snapshot

Once the lab is configured and tested:

1. Shut down the VM or save its state.
2. Open the VirtualBox Snapshots panel.
3. Create a snapshot of the clean environment.
4. Give it a descriptive name.

Recommended snapshot name:

`Clean Kali Linux - Initial Lab Setup`

This creates a restore point before running experiments or making major system changes.

---

## Lab Verification

| Test | Command | Expected Result |
|---|---|---|
| IP Address | `ip a` | IP address is displayed |
| Routing | `ip route` | Correct routing table is shown |
| Connectivity | `ping -c 4 8.8.8.8` | Successful ping replies |
| DNS Resolution | `nslookup google.com` | Domain resolves successfully |
| Nmap Verification | `nmap --version` | Version information is displayed |
| OS Verification | `cat /etc/os-release` | Kali Linux details are shown |

---

## Screenshots

The following screenshots show the VirtualBox environment and the Kali Linux desktop used in this lab setup.

<img width="834" height="506" alt="VirtualBox Environment" src="https://github.com/user-attachments/assets/7472b76b-631d-4302-97a7-cc5500fc463b" />

<img width="1361" height="669" alt="Kali Linux Desktop" src="https://github.com/user-attachments/assets/551493ba-e7fc-4cdd-8931-5de5bc344728" />

<!--
![VirtualBox Environment]()

![Kali Linux Desktop](screenshots/kali-desktop.png)

![Network Configuration](screenshots/terminal-ip.png)

![Connectivity Verification](screenshots/network-test.png)
-->

---

## Skills and Knowledge Gained

Through this project, I developed practical knowledge in:

- Virtualization and hypervisor configuration
- Kali Linux installation and Linux administration
- Virtual networking and connectivity troubleshooting
- IP addressing, routing, and DNS fundamentals
- Linux command-line usage and system verification
- Cybersecurity lab preparation and documentation
- Safe experimentation using snapshots and virtual environments

---

## Security and Ethical Use

This lab is intended strictly for educational purposes and authorized security testing.

All scanning, exploitation, and vulnerability assessment activities must only be performed on systems you own or have explicit permission to test. Ethical hacking begins with authorization, responsibility, and safe practice.

---

## References and Resources

- [Kali Linux Official Website](https://www.kali.org/)
- [Oracle VirtualBox](https://www.virtualbox.org/)
- [Nmap Documentation](https://nmap.org/book/)
- [Wireshark Documentation](https://www.wireshark.org/docs/)
- [Metasploit Documentation](https://docs.metasploit.com/)
- [OWASP](https://owasp.org/)

---

## Author

**Debela Beyena**

Cybersecurity Analyst | SOC Analyst

- GitHub: [@Debelabeyena2026](https://github.com/Debelabeyena2026)
- LinkedIn: [Connect with me](https://www.linkedin.com/)
- Email: dabeyhirpa2023@gmail.com

---

## Repository Summary

This repository documents a beginner-friendly cybersecurity lab setup created to help students understand how to build and validate a secure, isolated virtual environment. It is a practical introduction to virtualization, Linux administration, and networking fundamentals using Oracle VirtualBox and Kali Linux.

This project is ideal for academic work, portfolio development, and early hands-on practice in cybersecurity.

---

Thank you for visiting this project. Keep learning, stay curious, and practice cybersecurity responsibly.
