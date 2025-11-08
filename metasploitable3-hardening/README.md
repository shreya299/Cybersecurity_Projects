# 🛡️ Metasploitable 3 Hardening Project

## Overview
This project demonstrates the process of identifying, analyzing, and remediating vulnerabilities in a deliberately insecure virtual machine — **Metasploitable 3**.  
The objective was to perform a full vulnerability lifecycle: from **initial scanning** and **vulnerability discovery** to **fix implementation** and **post-fix validation**.

⚠️ *Note:* This project was conducted in a controlled academic lab environment for learning and ethical testing purposes.

---

## 🔍 Methodology
1. **Reconnaissance & Scanning**
   - Used **Nmap** for network scanning to identify open ports and running services.
   - Performed a **Nessus vulnerability scan** to detect outdated software and insecure configurations.

2. **Vulnerability Analysis**
   - Reviewed scan results to identify **critical and high-severity vulnerabilities** such as:
     - ProFTPD mod_copy Information Disclosure  
     - PhpMyAdmin SQL Injection  
     - Drupal Deserialization RCE  
     - SSH Weak Ciphers  
     - SMB Signing Not Required  

3. **Fix Implementation**
   - Upgraded and reconfigured affected services:
     - **FTP (ProFTPD)** → Updated to 1.3.5a+ to fix mod_copy issue.  
     - **SSH** → Restricted to strong ciphers and MACs only.  
     - **PhpMyAdmin** → Updated to latest stable version to patch SQLi.  
     - **Drupal Coder Module** → Disabled vulnerable versions and deployed latest.  
     - **SMB** → Configured to require client and server signatures.  
     - **PHP** → Upgraded from unsupported version.  
     - **Web Directories** → Disabled directory listing.  

4. **Post-Fix Verification**
   - Conducted another Nessus scan to validate remediations.
   - Verified reduction in vulnerabilities and improvement in **security posture**.

---

## 🧰 Tools & Technologies
| Category | Tools |
|-----------|--------|
| Scanning & Assessment | Nessus, Nmap |
| Configuration | Apache, PHP, SSH, Samba |
| Operating System | Metasploitable 3 (Ubuntu-based) |
| Documentation | Microsoft Word, PDF Reports |

---

## 📊 Results Summary
| Stage | Critical | High | Medium | Low |
|--------|-----------|------|--------|-----|
| **Before Fix** | 6 | 3 | 4 | 2 |
| **After Fix** | 1 | 1 | 2 | 2 |

✅ **Overall Vulnerability Reduction:** 60–70% improvement  
✅ **Security Posture Enhanced:** Services hardened, weak configurations removed

## 📖 Key Takeaways
- Strengthened skills in **vulnerability management** and **system hardening**.  
- Gained experience with **Nessus**, **Nmap**, and manual configuration hardening.  
- Learned the importance of continuous monitoring and patch validation.
