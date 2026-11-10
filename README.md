# Networkwalks B084 — Cybersecurity Week 1 Lab Setup

A hands-on virtual cybersecurity lab built with Oracle VirtualBox and Kali Linux. This project provides a secure, isolated environment for learning ethical hacking fundamentals, network analysis, and cybersecurity operations in a controlled setting.

## Overview

This lab demonstrates how to create a functional cybersecurity environment on a host machine by installing Oracle VirtualBox, deploying Kali Linux as a virtual machine, configuring networking, and validating the setup for future security exercises.

The project is designed to serve as a foundation for later penetration-testing labs, network reconnaissance, security monitoring, and red-team/blue-team experimentation in a safe and isolated environment.

---

## Project Objectives

- Install and configure Oracle VirtualBox on the host system.
- Deploy Kali Linux as a virtual machine.
- Allocate appropriate CPU, memory, and storage resources.
- Configure virtual networking for lab communication.
- Verify operating system, network, and internet connectivity.
- Create a clean virtual machine snapshot for recovery.
- Prepare a reusable environment for future cybersecurity activities.

---

## Lab Architecture

```text
+--------------------------------------+
|          Host Machine                |
|          Windows 10 / 11             |
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
|  Ethical Hacking & Security Testing |
+--------------------------------------+
```

### Lab Components

| Component | Description |
|---|---|
| Host Operating System | Windows-based machine running the virtualization environment |
| Hypervisor | Oracle VirtualBox |
| Guest Operating System | Kali Linux |
| Purpose | Learning cybersecurity, networking, and ethical hacking |
| Network Environment | Virtualized lab network |
| Tools | Nmap, Wireshark, Metasploit, Linux networking utilities |
| Security Model | Isolated and controlled environment |

---

## Technologies and Tools

| Tool | Purpose |
|---|---|
| Kali Linux | Penetration testing and security assessment |
| Oracle VirtualBox | Virtual machine creation and management |
| Nmap | Network discovery and port scanning |
| Wireshark | Packet capture and network traffic analysis |
| Metasploit Framework | Security testing and exploitation practice |
| Windows | Host machine platform |

---

## Prerequisites

Before starting the lab, make sure the following are available:

- A Windows host machine with sufficient system resources
- Oracle VirtualBox installed
- A valid Kali Linux ISO or virtual appliance image
- Enough RAM and storage for the virtual machine
- Internet access to download tools and OS images
- Administrative privileges on the host machine

---

## Step-by-Step Lab Setup

### Step 1: Install Oracle VirtualBox

Download and install the latest version of Oracle VirtualBox from the official site:

- Oracle VirtualBox Downloads: https://www.virtualbox.org/wiki/Downloads

### Step 2: Download Kali Linux

Download the official Kali Linux ISO or a ready-to-use VirtualBox image from the official project website:

- Kali Linux Downloads: https://www.kali.org/get-kali/

### Step 3: Extract the Virtual Machine Archive

If the Kali image is compressed, extract it using a file archiver such as 7-Zip before importing it into VirtualBox.

- 7-Zip: https://www.7-zip.org/

### Step 4: Import Kali Linux into VirtualBox

1. Open Oracle VirtualBox.
2. Select File → Import Appliance if using an OVA file.
3. Alternatively, create a new VM and attach the Kali ISO or import the existing virtual machine files.
4. Review and adjust the VM settings as needed.
5. Start the Kali Linux virtual machine.

### Step 5: Configure Virtual Machine Resources

Allocate resources based on your host machine's capacity and the intended lab workload.

| Resource | Recommended Configuration |
|---|---|
| Memory (RAM) | Based on host capacity; typically 2–8 GB |
| CPU Cores | Based on available host CPU resources |
| Virtual Disk | Kali Linux virtual disk image |
| Network Adapter | VirtualBox networking mode |
| Graphics Memory | Adjust to improve display performance |

### Step 6: Configure Network Connectivity

Set up the VM network adapter to match your lab goals.

Available VirtualBox networking modes include:

- NAT: Provides outbound internet access through the host.
- NAT Network: Allows communication with multiple virtual machines and outbound access.
- Host-Only Adapter: Connects the host and guest systems directly.
- Internal Network: Creates a private virtual network between VMs.

For security labs, an isolated or dedicated virtual network is recommended.

### Step 7: Verify Kali Linux Installation

Open a terminal in Kali Linux and run the following commands:

```bash
# Show network interfaces and IP addresses
ip a

# Show routing information
ip route

# Test internet connectivity
ping -c 4 8.8.8.8

# Verify DNS resolution
nslookup google.com

# Check Nmap installation
nmap --version

# Display OS information
cat /etc/os-release
```

### Step 8: Create a Snapshot

Once the base environment is working correctly:

1. Shut down the VM or save its state.
2. Open the VirtualBox Snapshots panel.
3. Create a snapshot of the clean lab environment.
4. Name it clearly for future recovery.

Recommended snapshot name:

`Clean Kali Linux - Initial Lab Setup`

Snapshots provide a safe restore point before making configuration changes or running experiments.

---

## Lab Verification

| Test | Command | Expected Result |
|---|---|---|
| IP Address | `ip a` | IP address is displayed |
| Routing | `ip route` | Correct routing table is shown |
| Connectivity | `ping -c 4 8.8.8.8` | Successful replies from the remote host |
| DNS Resolution | `nslookup google.com` | Domain resolves successfully |
| Nmap Verification | `nmap --version` | Version details are displayed |
| OS Verification | `cat /etc/os-release` | Kali Linux release information is shown |

---

## Lab Screenshots

These screenshots show the VirtualBox environment and the Kali Linux desktop used for the lab setup.

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

This project helped strengthen practical understanding in the following areas:

- Virtualization and hypervisor configuration
- Kali Linux installation and Linux administration
- Virtual network design and connectivity
- IP addressing, routing, and troubleshooting
- Command-line operations in Linux environments
- Cybersecurity lab setup and documentation
- Safe experimentation using virtual machines and snapshots

---

## Security and Ethical Use

This laboratory is intended strictly for educational purposes and authorized security testing.

All scanning, exploitation, and vulnerability assessment activities must be performed only on systems that you own or have explicit written permission to test. Ethical hacking begins with authorization, transparency, and responsible disclosure.

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

This repository documents a foundational cybersecurity lab setup designed to help learners understand how a secure virtual environment is created, configured, and validated before executing practical security tasks.

It is an excellent starting point for students, beginners, and aspiring SOC or cybersecurity professionals who want to build a realistic lab environment on a personal machine.

---

Thank you for visiting this project. Stay curious, keep learning, and build responsibly.

