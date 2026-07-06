# Cyber Kill Chain

## Overview

The Cyber Kill Chain is a framework developed by Lockheed Martin to describe the stages an attacker typically follows during a cyber attack. By understanding each phase of the attack lifecycle, defenders can detect, disrupt, or prevent attacks before they reach their objective.

Rather than viewing an attack as a single event, the Cyber Kill Chain breaks it into a sequence of steps, allowing SOC analysts to identify where defensive controls can be applied.

---

# Learning Objectives

After completing this room, I can:

- Explain the purpose of the Cyber Kill Chain.
- Describe each phase of the attack lifecycle.
- Understand how defenders can disrupt attacks at different stages.
- Relate the framework to incident detection and response.

---

# Why the Cyber Kill Chain Matters

Cyber attacks rarely happen instantly.

Attackers typically perform reconnaissance, deliver malicious payloads, establish persistence, and achieve their objectives over multiple stages.

Understanding these stages helps defenders:

- Detect attacks earlier.
- Identify attacker objectives.
- Improve defensive controls.
- Reduce incident impact.

---

# The Seven Stages

## 1. Reconnaissance

The attacker gathers information about the target.

Examples:

- Searching public websites
- LinkedIn research
- DNS enumeration
- Employee information gathering

### Defensive Measures

- Security awareness
- Limit exposed information
- External attack surface monitoring

---

## 2. Weaponization

The attacker prepares the malicious payload.

Examples:

- Creating phishing documents
- Embedding malware
- Preparing exploit kits

### Defensive Measures

Although difficult to detect directly, organizations reduce risk through patching and user awareness.

---

## 3. Delivery

The attacker delivers the payload.

Examples:

- Phishing emails
- Malicious websites
- USB devices
- Drive-by downloads

### Defensive Measures

- Email filtering
- Web filtering
- User awareness training
- Attachment scanning

---

## 4. Exploitation

The malicious payload executes by exploiting a vulnerability.

Examples:

- Office macro execution
- Software vulnerabilities
- Browser exploits

### Defensive Measures

- Patch management
- Endpoint protection
- Application control

---

## 5. Installation

The attacker installs malware or establishes persistence.

Examples:

- Registry Run Keys
- Scheduled Tasks
- Services
- Startup folders

### Defensive Measures

- EDR
- Application allowlisting
- Endpoint monitoring

---

## 6. Command and Control (C2)

The compromised system communicates with the attacker's infrastructure.

Examples:

- HTTPS
- DNS tunneling
- Reverse shells
- Beaconing

### Defensive Measures

- Firewall monitoring
- DNS monitoring
- Network detection
- Proxy monitoring

---

## 7. Actions on Objectives

The attacker achieves their goal.

Examples:

- Data theft
- Ransomware deployment
- Credential theft
- Lateral movement
- Destruction of systems

### Defensive Measures

- Incident response
- Backups
- Network segmentation
- Continuous monitoring

---

# Cyber Kill Chain Summary

| Stage | Goal |
|--------|------|
| Reconnaissance | Gather information |
| Weaponization | Prepare attack |
| Delivery | Deliver payload |
| Exploitation | Execute malicious code |
| Installation | Establish persistence |
| Command & Control | Communicate with attacker |
| Actions on Objectives | Achieve attacker goals |

---

# Real-World Example

An attacker targets a company employee.

1. Collects employee information from LinkedIn.
2. Creates a phishing email with a malicious attachment.
3. Sends the email.
4. The employee opens the attachment.
5. Malware installs itself.
6. The infected device communicates with the attacker's server.
7. The attacker steals company data.

Each step represents a stage in the Cyber Kill Chain where defenders have opportunities to detect or stop the attack.

---

# Practical Skills Developed

During this room I learned:

- Understanding attack lifecycles.
- Mapping attacker behaviour.
- Identifying defensive opportunities.
- Thinking proactively about detection and prevention.

---

# Key Terminology

| Term | Description |
|------|-------------|
| Reconnaissance | Information gathering before an attack. |
| Delivery | Sending the malicious payload. |
| Exploitation | Triggering malicious code execution. |
| Persistence | Maintaining long-term access to a system. |
| Command and Control (C2) | Communication between compromised systems and attackers. |

---

# Interview Questions

## What is the Cyber Kill Chain?

The Cyber Kill Chain is a framework that describes the stages of a cyber attack, helping defenders understand and interrupt attacker activities.

---

## Why is the Cyber Kill Chain useful?

It allows defenders to detect attacks at different stages and implement controls that prevent attackers from progressing through the attack lifecycle.

---

## Which stage is phishing?

Phishing is typically part of the **Delivery** stage.

---

## Which stage involves malware communicating with the attacker?

The **Command and Control (C2)** stage.

---

# Connections to My Home Lab

This framework connects directly to my home lab:

- pfSense firewall logs can help identify Command and Control traffic.
- Windows Event Logs can reveal exploitation and persistence.
- Active Directory logs can show authentication attempts and lateral movement.
- Future SIEM deployments can correlate events across multiple stages of the kill chain.

Understanding the Cyber Kill Chain helps me think about how different systems in my lab could contribute to detecting attacks throughout their lifecycle.

---

# Key Takeaways

- Cyber attacks follow a sequence of stages.
- Defenders can interrupt attacks at multiple points.
- Early detection reduces the overall impact of an attack.
- The framework supports structured incident investigations.

---

# Personal Reflection

Before completing this room, I mainly viewed cyber attacks as isolated events.

After completing it, I understand that attacks are a sequence of connected stages. This framework has helped me think more systematically about where security controls can detect or disrupt an attacker before they achieve their objectives.
