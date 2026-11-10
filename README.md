
NETWORKWALKS-B084-WK1-PM1-CYBERSECURITY-LAB-SETUP
---

     **Summary**
This project demonstrates the installation and configuration of a virtual cybersecurity laboratory using **Oracle VirtualBox and Kali Linux**.The lab provides a secure, isolated, and flexible virtual environment for learning cybersecurity fundamentals, practicing ethical hacking, exploring penetration-testing tools, and conducting hands-on security experiments.The primary objective is to build a practical cybersecurity lab that can be expanded with additional virtual machines to simulate real-world attack and defense scenarios, perform vulnerability assessments, analyze security threats, and strengthen practical cybersecurity skills.
This project serves as a foundation for future cybersecurity experiments, penetration-testing exercises, and security operations training in a controlled environment.

---

##       Project Objectives

- Install and configure Oracle VirtualBox.
- Deploy Kali Linux as a virtual machine.
- Configure virtual machine hardware resources.
- Establish virtual network connectivity.
- Verify system and network functionality.
- Create a clean VM snapshot for recovery.
- Prepare a foundation for future cybersecurity projects.

---



##           Lab Architecture

```text
+----------------------------------+
|        Host Machine              |
|          Windows 10               |
+----------------------------------+
                 |
                 v
+----------------------------------+
|          Hypervisor              |
|       Oracle VirtualBox          |
+----------------------------------+
                 |
                 v
+----------------------------------+
|       Virtual Machine            |
|         Kali Linux               |
+----------------------------------+
                 |
                 v
+----------------------------------+
|     Cybersecurity Lab            |
|   Ethical Hacking Environment    |
+----------------------------------+
```



###       Lab Components

| Component | Description |
|---|---|
| Host Operating System | Windows |
| Hypervisor | Oracle VirtualBox |
| Virtual Machine | Kali Linux |
| Lab Purpose | Cybersecurity & Ethical Hacking |
| Network Environment | Virtual Network |
| Security Tools | Nmap, Wireshark, Metasploit |
| Environment Type | Isolated Virtual Lab |

---

##   Technologies & Tools

| Tool | Purpose |
|---|---|
|   Kali Linux | Penetration testing and security assessment |
|   Oracle VirtualBox | Virtual machine management |
|   Nmap | Network discovery and port scanning |
|   Wireshark | Network traffic analysis |
|   Metasploit Framework | Security testing and exploitation practice |
|   Windows | Host operating system |

---

##  Lab Setup Procedure

### Step 1: Install Oracle VirtualBox

Download and install Oracle VirtualBox on the host machine.

🔗 https://www.virtualbox.org/wiki/Downloads

### Step 2: Download Kali Linux

Download the pre-built Kali Linux VirtualBox image from the official website.

🔗 https://www.kali.org/get-kali/

### Step 3: Extract the Virtual Machine

Use 7-Zip to extract the downloaded Kali Linux archive if required.

🔗 https://www.7-zip.org/

### Step 4: Import Kali Linux into VirtualBox

1. Open Oracle VirtualBox.
2. Select **File → Import Appliance**, if using an OVA file.
3. Alternatively, add the existing VM using its `.vbox` configuration file.
4. Review the virtual machine configuration.
5. Start the Kali Linux virtual machine.

### Step 5: Configure Virtual Machine Resources

Allocate appropriate hardware resources based on the host machine's available capacity.

| Resource | Configuration |
|---|---|
| Memory (RAM) | Based on host capacity |
| CPU Cores | Based on host capacity |
| Virtual Disk | Kali Linux virtual disk |
| Network Adapter | VirtualBox network mode |
| Graphics Memory | Adjusted for VM performance |

### Step 6: Configure Network Connectivity

Configure the virtual network adapter according to the lab requirements.

Available network modes include:

- **NAT:** Provides outbound connectivity through the host.
- **NAT Network:** Allows communication between connected VMs and outbound connectivity.
- **Host-Only Adapter:** Creates communication between the host and virtual machines.
- **Internal Network:** Creates an isolated network between virtual machines.

For security testing, an isolated or dedicated virtual network is recommended.

### Step 7: Verify Kali Linux

Open the Kali Linux terminal and execute the following commands.

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

### Step 8: Create a Virtual Machine Snapshot

After completing the initial setup:

1. Shut down or save the VM state as appropriate.
2. Open the VirtualBox Snapshots section.
3. Create a snapshot of the clean environment.
4. Give it a descriptive name.

**Recommended snapshot name:**

`Clean Kali Linux - Initial Lab Setup`

Snapshots provide a recovery point before performing experiments or making significant system changes.

---

## 🔍 Lab Verification

| Test | Command | Expected Result |
|---|---|---|
| IP Address | `ip a` | IP address displayed |
| Routing | `ip route` | Correct routing table |
| Connectivity | `ping -c 4 8.8.8.8` | Successful replies |
| DNS Resolution | `nslookup google.com` | Domain resolves |
| Nmap Verification | `nmap --version` | Version information displayed |
| OS Verification | `cat /etc/os-release` | Kali Linux details displayed |

---

##  Lab Screenshots



<!-- Add screenshots to your repository and uncomment the examples below -->
<img width="834" height="506" alt="VB" src="https://github.com/user-attachments/assets/7472b76b-631d-4302-97a7-cc5500fc463b" />
<img width="1361" height="669" alt="Kali linux" src="https://github.com/user-attachments/assets/551493ba-e7fc-4cdd-8931-5de5bc344728" />



<!--
![VirtualBox Environment]()

![Kali Linux Desktop](screenshots/kali-desktop.png)

![Network Configuration](screenshots/terminal-ip.png)

![Connectivity Verification](screenshots/network-test.png)
-->

---

##   Skills & Knowledge Gained

Through this hands-on project, I strengthened my understanding of:

- Virtualization and hypervisor configuration.
- Kali Linux installation and administration.
- Virtual network architecture and connectivity.
- IP addressing, subnetting, and routing fundamentals.
- Linux command-line operations.
- Cybersecurity lab preparation and documentation.
- Safe experimentation using virtual machines and snapshots.

---

##  Security & Ethical Use

This laboratory is designed exclusively for **educational purposes and authorized security testing**.

All scanning, exploitation, and vulnerability assessment activities must be conducted only against systems that I own or have explicit permission to test.

**Ethical hacking begins with authorization and responsible disclosure.**

---

##   References & Resources

- [Kali Linux Official Website](https://www.kali.org/)
- [Oracle VirtualBox](https://www.virtualbox.org/)
- [Nmap Documentation](https://nmap.org/book/)
- [Wireshark Documentation](https://www.wireshark.org/docs/)
- [Metasploit Documentation](https://docs.metasploit.com/)
- [OWASP](https://owasp.org/)

---

##   Author

      **Debela Beyena**

      Cybersecurity Analyst | SOC Analyst |

- GitHub: [@Debelabeyena2026](https://github.com/Debelabeyena2026)
- LinkedIn: [Connect with me](https://www.linkedin.com/) Gmail:dabeyhirpa2023@gmail.com

---

