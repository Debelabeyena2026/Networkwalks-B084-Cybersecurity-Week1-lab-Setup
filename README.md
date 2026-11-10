# Networkwalks B084 — Cybersecurity Week 1 Lab Setup

A beginner-friendly virtual cybersecurity lab built with Oracle VirtualBox and Kali Linux. This project helps students learn how to configure a safe, isolated lab environment for practicing network analysis, Linux administration, and ethical hacking fundamentals.

## Overview

This repository documents the setup of a cybersecurity lab using a host machine, Oracle VirtualBox, and a Kali Linux virtual machine. The goal is to provide a practical learning environment for students to explore cybersecurity concepts in a controlled and secure way.

This project is ideal for beginners who want to understand virtualization, networking, Linux command-line tools, and ethical security testing without affecting a real production environment.

---

## Why This Repository Is a Good Student Project

This repository is a strong student project because it demonstrates:

- Practical hands-on cybersecurity learning
- Real-world virtualization setup using VirtualBox
- Linux-based network troubleshooting and system verification
- Safe experimentation in an isolated environment
- Clear documentation and step-by-step guidance
- A foundation for future labs in networking, ethical hacking, and SOC analysis

---

## Learning Objectives

By completing this lab, students will be able to:

- Install and configure Oracle VirtualBox
- Deploy Kali Linux in a virtual environment
- Allocate system resources for a VM
- Configure virtual networking modes
- Verify IP configuration, routing, and DNS
- Validate connectivity using practical Linux commands
- Create recovery snapshots for safe experimentation

---

## Lab Architecture

```text
+--------------------------------------+
|          Host Machine                |
|      Windows 10 / 11 or similar      |
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
|   Ethical Hacking & Security Tools  |
+--------------------------------------+
```

### Lab Components

| Component | Description |
|---|---|
| Host Operating System | Machine used to run the virtual lab |
| Hypervisor | Oracle VirtualBox |
| Guest Operating System | Kali Linux |
| Purpose | Cybersecurity learning and ethical testing |
| Network Environment | Isolated virtual networking |
| Tools | Nmap, Wireshark, Metasploit, Linux utilities |
| Security Model | Controlled and safe environment |

---

## Technologies and Tools

| Tool | Purpose |
|---|---|
| Kali Linux | Penetration testing and security analysis |
| Oracle VirtualBox | Virtual machine management |
| Nmap | Network discovery and port scanning |
| Wireshark | Packet capture and traffic analysis |
| Metasploit Framework | Vulnerability testing and exploitation practice |
| Windows | Host environment |

---

## Prerequisites

Before starting the lab, ensure the following are available:

- A capable Windows host machine
- Oracle VirtualBox installed
- A Kali Linux ISO or prebuilt VM image
- Sufficient RAM and disk space for the VM
- Internet access for downloading tools and images
- Administrative access to the host machine

---

## Step-by-Step Setup Guide

### Step 1: Install Oracle VirtualBox

Download the latest version of Oracle VirtualBox from the official website:

- Oracle VirtualBox Downloads: https://www.virtualbox.org/wiki/Downloads

### Step 2: Download Kali Linux

Get the official Kali Linux ISO or VirtualBox-ready image:

- Kali Linux Downloads: https://www.kali.org/get-kali/

### Step 3: Extract the Downloaded Files

If the archive is compressed, use a utility such as 7-Zip to extract it before use.

- 7-Zip: https://www.7-zip.org/

### Step 4: Import Kali Linux into VirtualBox

1. Open Oracle VirtualBox.
2. Select File → Import Appliance if using an OVA file.
3. Alternatively, create a new VM and attach the downloaded ISO.
4. Review the VM settings.
5. Start the Kali Linux machine.

### Step 5: Configure Virtual Machine Resources

Adjust the machine resources based on the host system and expected lab usage.

| Resource | Recommended Configuration |
|---|---|
| Memory (RAM) | Based on host capacity; typically 2–8 GB |
| CPU Cores | Based on available host CPU resources |
| Virtual Disk | Kali Linux disk image |
| Network Adapter | VirtualBox network mode |
| Graphics Memory | Adjust depending on display needs |

### Step 6: Configure Network Connectivity

Choose an appropriate VirtualBox networking mode for your lab:

- NAT: Internet access through the host
- NAT Network: Communication between virtual machines and outbound access
- Host-Only Adapter: Communication between host and guest systems
- Internal Network: Isolated VM-to-VM network

For cybersecurity labs, a dedicated or isolated network is recommended.

### Step 7: Verify the Kali Linux Setup

Open a terminal and run the following commands:

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

# Display OS information
cat /etc/os-release
```

### Step 8: Create a Snapshot

After the base setup works correctly:

1. Shut down the VM or save its state.
2. Open the VirtualBox Snapshots section.
3. Create a snapshot of the clean environment.
4. Give it a clear and descriptive name.

Recommended snapshot name:

`Clean Kali Linux - Initial Lab Setup`

This gives you a secure restore point before running experiments or modifying system settings.

---

## Lab Verification

| Test | Command | Expected Result |
|---|---|---|
| IP Address | `ip a` | IP address is displayed |
| Routing | `ip route` | Correct routing table is shown |
| Connectivity | `ping -c 4 8.8.8.8` | Successful response from destination |
| DNS Resolution | `nslookup google.com` | Domain resolves correctly |
| Nmap Verification | `nmap --version` | Version information is displayed |
| OS Verification | `cat /etc/os-release` | Kali Linux details are shown |

---

## Screenshots

The screenshots below show the VirtualBox environment and the Kali Linux desktop used for the lab setup.

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

This project helps students build foundational skills in:

- Virtualization and hypervisor configuration
- Kali Linux installation and administration
- Virtual networking and connectivity troubleshooting
- IP addressing, routing, and DNS fundamentals
- Linux command-line usage
- Ethical cybersecurity lab preparation
- Safe experimentation with snapshots and recovery points

---

## Security and Ethical Use

This laboratory is intended strictly for educational purposes and authorized security testing.

All scanning, exploitation, and vulnerability assessment activities must be performed only on systems that you own or have explicit permission to test. Ethical hacking begins with authorization, responsibility, and safe practice.

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

This repository is a hands-on beginner project that teaches students how to build and validate a cybersecurity lab environment. It is designed as a practical introduction to virtualization, network configuration, Linux troubleshooting, and ethical security testing.

It is a strong student repository because it combines clear documentation, useful lab steps, real-world tools, and an applied learning workflow.

---

Thank you for visiting this project. Keep learning, stay curious, and practice cybersecurity responsibly.
