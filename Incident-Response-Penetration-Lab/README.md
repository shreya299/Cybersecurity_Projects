# Incident Response & Penetration Testing Lab

![Domain](https://img.shields.io/badge/Domain-Cybersecurity-blue?style=for-the-badge)
![Type](https://img.shields.io/badge/Type-Lab%2FExercise-lightgrey?style=for-the-badge)
![Tools](https://img.shields.io/badge/Tools-Nmap%2C%20Metasploit%2C%20Wireshark%2C%20Nessus-orange?style=for-the-badge)

## Overview
This project simulates a full cybersecurity engagement — from vulnerability assessment and penetration testing to incident detection and response.  
It was performed in a controlled home lab environment using intentionally vulnerable machines (**Metasploitable** and **Bee-Box**) to practice reconnaissance, exploitation, monitoring, and post-incident remediation.

---

## Project Components

### 1) Vulnerability Assessment — RED Team  
**File:** [vulnerability assessment report_RED Team.pdf](./vulnerability%20assessment%20report_RED%20Team.pdf)  
- Conducted reconnaissance and scanning using **Nmap** and **OpenVAS/Nessus**.  
- Discovered and categorized vulnerabilities across Metasploitable and Bee-Box.  
- Notable issues: outdated software, directory traversal, SSL/TLS misconfigurations, DoS exposures, and **ProFTPD mod_copy (CVE-2015-3306)**.  
- Mapped findings to CVE IDs and CVSS scores for prioritization.

---

### 2) Penetration Test — RED Team  
**File:** [Pentest_Report_RED Team.pdf](./Pentest_Report_RED%20Team.pdf)  
- Performed controlled exploitation using **Metasploit** to validate critical vulnerabilities.  
- Demonstrated code execution and reverse shells via the **ProFTPD mod_copy exploit (CVE-2015-3306)**.  
- Executed SSH authentication and privilege-escalation testing.  
- Recommended mitigations: patching, network segmentation, and stronger authentication mechanisms.

---

### 3) Incident Report & Response — BLUE Team  
**Files:**  
- [Incident Report.pdf](./Incident%20Report.pdf) — Blue Team evidence and findings (packet captures, logs, and host analysis).  
- [Incident Response Plan.pdf](./Incident%20Response%20Plan.pdf) — Formal playbook: containment, eradication, recovery, communication, and lessons learned.

**Summary:**  
- The Blue Team used **Wireshark** to monitor network traffic, detect suspicious activity, and correlate events with Red Team activity.  
- Incident response actions included host isolation, vulnerability remediation, and log analysis.  
- Deliverables: a sanitized **Incident Report** (evidence + analysis) and an actionable **Incident Response Plan (IRP)**.

---

## How to use this repository
1. Review the **Vulnerability Assessment Report** to understand baseline weaknesses.  
2. Read the **Penetration Test Report** to explore exploit paths and validation steps.  
3. Refer to the **Incident Report** and **Incident Response Plan** for mitigation and post-incident learning.

---
