# Network Scanning & Enumeration Lab (Nmap)

## Objective
This lab demonstrates hands-on network scanning and enumeration using **Nmap** in a self-built, controlled virtual environment. The goal was to identify live hosts, enumerate open ports and services, and gather system information relevant to IT support and SOC investigations.

---

## Lab Environment
- Host OS: Ubuntu Linux
- Virtualization: VirtualBox
- Network Type: Local virtual subnet (Ubuntu Server)
- Tools Used:
  - Nmap
  - Linux CLI

---

## Lab Overview
Before performing any scans, basic network connectivity and host availability were verified. Scans were then progressively expanded to gather more detailed information, simulating a real-world enumeration workflow used in IT troubleshooting and security monitoring.

---

## Methodology & Findings

### 1. Network Verification & Host Discovery
The lab began by confirming network configuration and target availability.

Actions performed:
- Verified local IP address using `ip a`
- Confirmed connectivity to the target host using `ping`
- Performed host discovery using `nmap -sn`

This confirmed that the target system was reachable and active on the network.

📸 **Screenshot:** `screenshots/nmap_host_discovery.png`

---

### 2. Port Scanning & Service Enumeration
After confirming host availability, port scanning was performed to identify exposed services.

Actions performed:
- Default TCP port scan
- Service and version detection using `nmap -sV`

Key findings:
- Open ports identified:
  - 21/tcp (FTP)
  - 22/tcp (SSH)
  - 80/tcp (HTTP)
- Services detected:
  - vsftpd
  - OpenSSH
  - Apache HTTP Server

These results provide visibility into services that could represent potential security risks if misconfigured or unpatched.

📸 **Screenshot:** `screenshots/nmap_port_scan.png`

---

### 3. OS Detection & Advanced Enumeration
To gather additional system-level details, more advanced scans were performed.

Actions performed:
- OS detection using `nmap -O`
- Aggressive scan using `nmap -A`
- Full port scan using `nmap -p-`

Key findings:
- Target identified as a Linux-based system
- Additional service and system fingerprinting data collected
- Network distance and traceroute information gathered

These techniques demonstrate how deeper enumeration supports incident response, asset identification, and vulnerability analysis.

📸 **Screenshot:** `screenshots/nmap_os_detection.png`

---

## Results Summary
- Successfully identified a live host on the network
- Enumerated open ports and running services
- Detected service versions and operating system characteristics
- Demonstrated a structured approach to network enumeration

---

## Key Takeaways
- Asset discovery is a foundational step in both IT operations and security monitoring
- Exposed services increase attack surface if not properly managed
- Layered scanning techniques provide progressively deeper visibility
- Clear documentation supports troubleshooting and incident response

---

## Next Steps
- Perform UDP scanning for additional service discovery
- Correlate scan results with simulated SIEM alerts
- Conduct vulnerability scanning against identified services
