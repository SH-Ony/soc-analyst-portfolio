# MITRE ATT&CK Framework

## Overview

MITRE ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge) is a globally recognized knowledge base that documents how real-world attackers behave after gaining access to a system.

Unlike frameworks that describe the stages of an attack, MITRE ATT&CK focuses on the specific tactics and techniques adversaries use during an intrusion. It enables defenders to understand attacker behavior, improve detections, perform threat hunting, and strengthen incident response.

MITRE ATT&CK has become one of the most widely used frameworks in Security Operations Centers (SOCs), threat hunting, detection engineering, and red and blue team exercises.

---

# Learning Objectives

After completing this room, I can:

- Explain the purpose of the MITRE ATT&CK framework.
- Understand the difference between tactics and techniques.
- Navigate the ATT&CK Matrix.
- Describe how SOC analysts use MITRE during investigations.
- Relate attacker behavior to defensive detections.

---

# Why MITRE ATT&CK Matters

Security tools generate alerts.

MITRE ATT&CK helps analysts answer questions such as:

- What is the attacker trying to achieve?
- Which technique was used?
- What stage of the attack does this represent?
- Which detections are missing?
- How can similar attacks be detected in the future?

Rather than focusing on malware names, MITRE focuses on attacker behaviour.

---

# What is the ATT&CK Matrix?

The ATT&CK Matrix organizes attacker behavior into **Tactics** and **Techniques**.

Think of it like this:

**Tactic = Why the attacker is performing an action.**

**Technique = How the attacker performs that action.**

Example:

Tactic:

- Credential Access

Technique:

- Credential Dumping

The attacker wants credentials (tactic).

They use credential dumping (technique).

---

# Common ATT&CK Tactics

Some of the most common tactics include:

- Initial Access
- Execution
- Persistence
- Privilege Escalation
- Defense Evasion
- Credential Access
- Discovery
- Lateral Movement
- Collection
- Command and Control
- Exfiltration
- Impact

Each tactic represents a specific attacker objective.

---

# Techniques

Each tactic contains one or more techniques.

Examples include:

### Initial Access

- Phishing
- Exploiting Public-Facing Applications
- Valid Accounts

---

### Execution

- PowerShell
- Command Shell
- Scheduled Tasks

---

### Persistence

- Registry Run Keys
- Services
- Startup Folder

---

### Credential Access

- Credential Dumping
- Brute Force

---

### Lateral Movement

- Remote Desktop Protocol (RDP)
- SMB
- PsExec

---

### Command and Control

- Web Protocols
- DNS
- HTTPS

---

# How SOC Analysts Use MITRE

SOC analysts use MITRE ATT&CK to:

- Investigate alerts.
- Classify attacker activity.
- Build detection rules.
- Perform threat hunting.
- Improve SIEM use cases.
- Communicate findings consistently.

MITRE provides a common language for security teams.

---

# ATT&CK in a SOC Investigation

Example:

An alert shows suspicious PowerShell activity.

The analyst identifies:

Technique:

PowerShell

↓

Tactic:

Execution

↓

Additional logs reveal credential dumping.

↓

Credential Access

↓

Later, unusual RDP connections appear.

↓

Lateral Movement

Using MITRE ATT&CK, the analyst maps the entire attack path and understands how the attacker progressed through the environment.

---

# ATT&CK vs Cyber Kill Chain

| Cyber Kill Chain | MITRE ATT&CK |
|------------------|--------------|
| Describes attack stages | Describes attacker behaviour |
| High-level lifecycle | Detailed techniques |
| Seven stages | Hundreds of techniques |
| Focus on attack progression | Focus on detection and defence |

The two frameworks complement each other rather than replace one another.

---

# Real-World Example

A phishing email delivers malware to a workstation.

MITRE mapping:

| Activity | MITRE Tactic |
|-----------|--------------|
| Phishing email | Initial Access |
| PowerShell execution | Execution |
| Registry modification | Persistence |
| Credential dumping | Credential Access |
| RDP movement | Lateral Movement |
| Data theft | Exfiltration |

Mapping attacks like this helps defenders understand attacker behaviour and identify detection opportunities.

---

# Practical Skills Developed

During this room I learned:

- Navigating the ATT&CK Matrix.
- Understanding attacker behaviour.
- Mapping attacks to tactics and techniques.
- Thinking like a defender.
- Improving detection strategies.

---

# Key Terminology

| Term | Description |
|------|-------------|
| ATT&CK | Adversarial Tactics, Techniques, and Common Knowledge. |
| Tactic | The attacker's objective. |
| Technique | How the attacker achieves the objective. |
| Procedure | The specific implementation of a technique by an attacker. |
| ATT&CK Matrix | The collection of tactics and techniques organized into a framework. |

---

# Interview Questions

## What is MITRE ATT&CK?

MITRE ATT&CK is a knowledge base that documents real-world attacker tactics and techniques, helping defenders understand, detect, and respond to cyber threats.

---

## What is the difference between a tactic and a technique?

A tactic describes **why** an attacker performs an action, while a technique describes **how** that action is carried out.

---

## Why do SOC analysts use MITRE ATT&CK?

SOC analysts use MITRE ATT&CK to classify attacker behaviour, improve detections, investigate incidents, perform threat hunting, and communicate findings using a common framework.

---

## Does MITRE ATT&CK replace the Cyber Kill Chain?

No.

The Cyber Kill Chain focuses on the stages of an attack, while MITRE ATT&CK provides detailed information about attacker tactics and techniques. Both frameworks complement each other.

---

# Connections to My Home Lab

MITRE ATT&CK provides a useful framework for interpreting activity within my home lab.

Examples include:

- Windows Event Logs showing PowerShell execution.
- Active Directory authentication events.
- pfSense firewall logs revealing network communication.
- Future SIEM detections mapped to MITRE techniques.
- Security monitoring based on attacker behaviour rather than isolated Indicators of Compromise (IOCs).

As I continue building my home lab, I plan to map simulated attacks to the ATT&CK Matrix to better understand how different techniques appear in system and network logs.

---

# Key Takeaways

- MITRE ATT&CK focuses on attacker behaviour.
- Tactics describe objectives.
- Techniques describe how objectives are achieved.
- The framework helps analysts investigate, detect, and hunt threats.
- MITRE ATT&CK is widely used across modern SOC operations.

---

# Personal Reflection

Before completing this room, I knew that MITRE ATT&CK was a popular cybersecurity framework, but I did not fully understand how it was applied during investigations.

After completing this room, I now understand that MITRE ATT&CK provides a common language for describing attacker behaviour. Rather than focusing only on individual alerts, it helps analysts connect related activities, understand attacker objectives, and identify opportunities to improve future detections.
