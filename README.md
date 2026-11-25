
# Cybersecurity Trainee (Internship) – Preliminary Interview Test

## Overview

This repository contains my responses to the **Preliminary Interview Test for Cyber Security Trainee (Internship)**.

The assessment covers fundamental cybersecurity concepts, incident response procedures, threat detection, vulnerability assessment, risk management, and current developments in the cybersecurity industry.

The answers demonstrate my understanding of common cybersecurity scenarios and the practical steps involved in identifying, investigating, containing, and mitigating security threats.

## Table of Contents

1. [Phishing Email](#1-phishing-email)
2. [Malware Infection](#2-malware-infection)
3. [Ransomware Attack](#3-ransomware-attack)
4. [Unauthorized Access Attempt](#4-unauthorized-access-attempt)
5. [Data Breach Suspicion](#5-data-breach-suspicion)
6. [Web Application Vulnerability](#6-web-application-vulnerability)
7. [Network Compromise](#7-network-compromise)
8. [Risk Management and AI Security](#8-risk-management-and-ai-security)
9. [Security Checklist Exercise](#9-security-checklist-exercise)
10. [Current Affairs in Cybersecurity](#10-current-affairs-in-cybersecurity)

---

## 1. Phishing Email

**Question:**

An employee reports receiving an email asking them to "verify their account" by clicking a link. How would you confirm if this is a phishing attempt and what steps would you take to contain and report it?

**Answer:**

I would inspect the sender address, email headers (SPF, DKIM, DMARC results), and the link itself by hovering over it without clicking. I would then check the URL in a sandbox or on VirusTotal and look for urgency, spelling errors, and mismatched domains.

To contain it, I would tell the employee not to click or reply, and ask whether they already did. If they clicked or entered credentials, I would reset their password, revoke active sessions, and enable MFA.

I would block the sender and domain on the mail gateway, search all mailboxes for the same email and delete it, and add the URL to the web filter. Finally, I would report it to the security team, log the incident, and run awareness reminders for staff.

## 2. Malware Infection

**Question:**

A user's computer suddenly begins acting abnormally, running slowly, and displaying pop-up ads. How would you investigate and remediate this issue to ensure the malware is completely removed and the system is secured?

**Answer:**

I would first disconnect the machine from the network to stop the spread. Then I would check Task Manager, startup items, browser extensions, and scheduled tasks for suspicious entries.

I would run a full scan with updated antivirus and an anti-malware tool such as Malwarebytes, plus offline scanning in Safe Mode if needed. I would review logs to find how it got in (a download, email, or USB).

After removal, I would patch the OS and software, change the user's passwords, and monitor the machine for recurrence. If I can't be sure it is clean, I would reimage the machine and restore data from a verified clean backup.

## 3. Ransomware Attack

**Question:**

You discover that a server hosting company files has been encrypted, and ransom notes have appeared in multiple folders. What immediate steps would you take to respond to this situation?

**Answer:**

I would immediately isolate the server by unplugging it from the network, without powering it off, so memory evidence is preserved.

I would alert the incident response team and management, and check whether other systems or shares are affected. I would identify the ransomware strain from the ransom note and file extensions.

I would not pay the ransom, as that is not recommended and doesn't guarantee recovery. I would preserve logs and evidence for forensics, then find the entry point (phishing, RDP, vulnerability).

Once the threat is eliminated, I would restore from clean offline backups, reset all credentials, and report to the authorities and any regulators as required.

## 4. Unauthorized Access Attempt

**Question:**

Your intrusion detection system (IDS) logs show multiple failed login attempts from a foreign IP address. What steps would you take to analyze, block, and prevent future unauthorized attempts?

**Answer:**

I would analyze the IDS and authentication logs to see the targeted accounts, timing, frequency, and whether any attempt succeeded.

I would check the IP's reputation using tools like AbuseIPDB, VirusTotal, and Shodan. I would block the IP and range on the firewall, then check whether the targeted accounts were compromised and force password resets if needed.

To prevent future attempts, I would enforce account lockout policies, MFA, and strong passwords, and consider geo-blocking and rate limiting. I would also tune IDS alerts, keep monitoring, and document the incident.

## 5. Data Breach Suspicion

**Question:**

A client reports that their confidential files appear on a public forum. How would you verify if a breach occurred, contain the impact, and handle the communication process internally and externally?

**Answer:**

To verify, I would examine the posted files to confirm they are genuine and identify which data is exposed and where it came from. I would review access logs, DLP alerts, and recent user activity to trace the source (insider, compromised account, or third party).

To contain it, I would revoke compromised credentials, close the leak path, and request takedown of the forum post.

Internally, I would notify management, legal, and the incident response team. Externally, I would inform the client and, where required, regulators and affected individuals within legal timelines (e.g., NDPR in Nigeria or GDPR).

I would then document lessons learned and strengthen controls.

## 6. Web Application Vulnerability

**Question:**

You are tasked to review a company's e-commerce website (e.g., built on WordPress or PrestaShop). List key areas you would check for security vulnerabilities and mention tools you could use to perform the test.

**Answer:**

Key areas to check:

- Injection flaws (SQL injection) and cross-site scripting (XSS).
- Authentication, session management, and admin panel exposure.
- Outdated CMS core, plugins, and themes.
- Payment and checkout security, HTTPS/TLS configuration.
- File upload handling, access control, and security headers.
- Misconfigurations and exposed backup or configuration files.

**Tools:**

- WPScan (WordPress security assessment).
- Nikto (web server scanning).
- OWASP ZAP (web application security testing).
- Burp Suite (web traffic inspection and testing).
- Nmap (network and service discovery).
- SQLmap (SQL injection testing).
- SSL Labs (SSL/TLS configuration assessment).

## 7. Network Compromise

**Question:**

You suspect that a device on the company network has been compromised and is communicating with a suspicious IP. What tools and steps would you use to identify, isolate, and remediate the affected device?

**Answer:**

I would use Wireshark or tcpdump to inspect traffic, and review firewall, proxy, DNS, and SIEM logs to identify the device and the destination IP.

I would check the IP's reputation and use Nmap or the DHCP/ARP tables to locate the device.

For isolation, I would quarantine it by disabling its switch port or moving it to a quarantine VLAN.

Then I would run an EDR or antivirus scan, review processes and connections (netstat), and collect forensic evidence.

Remediation involves removing the malware or reimaging, patching, and resetting credentials. Finally, I would block the malicious IP and monitor for any further communication.

## 8. Risk Management and AI Security

**Question:**

Your company recently adopted an AI assistant to automate support tasks. Describe how you would perform a risk assessment for this AI system, and mention what "prompt injection" means in AI security.

**Answer:**

I would identify the AI system's assets, data flows, and what data it can access (customer data, internal systems).

Then I would identify threats such as:

- Data leakage.
- Prompt injection.
- Hallucinated or incorrect answers.
- Unauthorized access.
- Third-party vendor risk.

I would rate each risk by likelihood and impact, apply controls (access limits, input/output filtering, logging, human review, vendor assessment), and review the results regularly.

**What is Prompt Injection?**

Prompt injection is an attack where a malicious user, or hidden text in a document or webpage, feeds crafted instructions into an AI so it ignores its original rules, leaks data, or performs unintended actions.

## 9. Security Checklist Exercise

**Question:**

You have just deployed a web application (e.g., PrestaShop). List at least five key items that should appear on your application security checklist, and how you would test one of them.

**Answer:**

**Key Security Checklist Items:**

1. Keep the CMS, modules, and themes updated.
2. Enforce HTTPS/SSL.
3. Use strong passwords and MFA, and rename or restrict the admin URL.
4. Install a web application firewall (WAF) and maintain regular backups.
5. Validate inputs to prevent SQL injection and XSS.

**Testing Example – SQL Injection:**

I would enter test payloads such as `' OR 1=1--` into login and search fields, or run SQLmap or OWASP ZAP against them.

Any database error or unexpected behavior would indicate a potential vulnerability requiring further investigation.

*Note: Security testing should only be performed on systems for which permission has been granted.*

## 10. Current Affairs in Cybersecurity

**Question:**

Briefly state who the following people are and what they are known for in the technology or cybersecurity world:

a. Kevin Mitnick  
b. Eugene Kaspersky  
c. Linus Torvalds  
d. Bruce Schneier  
e. Parisa Tabriz

**Answer:**

**a. Kevin Mitnick:** A famous former hacker, known for social engineering, who later became a security consultant and author (*The Art of Deception*).

**b. Eugene Kaspersky:** Russian cybersecurity expert and founder of Kaspersky Lab, known for its antivirus software and threat research.

**c. Linus Torvalds:** Creator of the Linux kernel and the Git version control system.

**d. Bruce Schneier:** American cryptographer and security author, known for books on security and cryptography and for his widely read blog.

**e. Parisa Tabriz:** Google security leader, known as the "Security Princess," who led Chrome security and Project Zero-related security efforts.

---

## Conclusion

This assessment has strengthened my understanding of fundamental cybersecurity principles and the practical approaches used to handle common security incidents.

It covers important areas such as phishing detection, malware investigation, ransomware response, access control, data breach investigation, network security, web application testing, and AI security.

I recognize the importance of continuous learning, practical experience, proper documentation, and following established security procedures when working in cybersecurity.

---

**Assessment:** Preliminary Interview Test  
**Role:** Cybersecurity Trainee (Internship)  
**Focus Areas:** Incident Response | Threat Detection | Network Security | Vulnerability Assessment | Risk Management | AI Security
