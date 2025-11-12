# Incident Response & Penetration Testing Lab


## Overview
This project simulates a full cybersecurity engagement — from **vulnerability assessment** and **penetration testing** to **incident detection** and **response**.  
It was performed in a controlled lab environment using vulnerable machines (Metasploitable and Bee-Box) to practice reconnaissance, exploitation, monitoring, and post-incident remediation.

---

## Project Components

### 🧩 1. [Vulnerability Assessment Report](./vulnerability assessment report_RED Team.pdf)
- Conducted reconnaissance and scanning using **Nmap** and **OpenVAS**.  
- Discovered and categorized vulnerabilities by severity across Metasploitable and Bee-Box.  
- Identified issues including outdated software, **directory traversal**, **Slowloris DoS**, **SSL/TLS misconfigurations**, and **ProFTPD Mod_Copy (CVE-2015-3306)**.  
- Mapped vulnerabilities to **CVE IDs** and **CVSS scores** for documentation.

---

### 🧨 2. [Penetration Test Report](./Penetration_Test_Report.pdf)
- Performed exploitation using **Metasploit Framework**.  
- Achieved authenticated access and established **reverse shells** through ProFTPD exploit (CVE-2015-3306).  
- Conducted **SSH brute force** attempts to test password security and privilege escalation.  
- Documented exploitation flow: reconnaissance → scanning → exploitation → post-exploitation validation.  
- Recommended mitigations including **patching, network segmentation**, and **access control hardening**.

---

### 🛡️ 3. [Incident Response Report](./Incident_Response_Report.pdf)
- Simulated Blue Team response to a detected attack within the same lab.  
- Used **Wireshark** to capture and analyze network packets for suspicious behavior.  
- Investigated FTP and SSH exploitation attempts in live traffic.  
- Developed a full **Incident Response Plan (IRP)** including:
  - Quick containment & isolation of compromised hosts  
  - Patch management & remediation  
  - Incident coordination & communication plan  
  - Continuous monitoring & threat intelligence integration  
  - Lessons learned & improvement plan

---

## Key Learning Outcomes
- Hands-on experience across the **cyber kill chain** — from vulnerability discovery to post-incident mitigation.  
- Improved ability to analyze packet captures and correlate network activity with exploitation attempts.  
- Strengthened understanding of **SIEM workflows, patch management, and response documentation**.  
- Gained proficiency in **threat detection, risk prioritization**, and **system hardening** techniques.

---

## Sample Commands Used

```bash
# Nmap network reconnaissance
nmap -A -sV 10.0.69.0/24

# Metasploit ProFTPD mod_copy exploit
use exploit/unix/ftp/proftpd_modcopy_exec
set RHOST 10.0.69.10
run

# Wireshark packet filter example
tcp.port == 21 || tcp.port == 22
