# Unified Kill Chain

## Overview

The Unified Kill Chain (UKC) is a cybersecurity framework developed by Paul Pols that expands upon the traditional Cyber Kill Chain. It combines concepts from the Cyber Kill Chain and the MITRE ATT&CK framework to better represent modern cyber attacks.

Unlike the Cyber Kill Chain, which focuses on a single sequence of attack stages, the Unified Kill Chain recognizes that attackers often repeat phases, move laterally, establish persistence, and interact with multiple systems before achieving their objectives.

The framework helps defenders understand the complete attack lifecycle and identify opportunities to detect or disrupt attackers at every stage.

---

# Learning Objectives

After completing this room, I can:

- Explain the purpose of the Unified Kill Chain.
- Understand how it differs from the Cyber Kill Chain.
- Describe the phases of the framework.
- Explain how it supports threat detection and incident response.
- Recognize why it is useful for defending against modern attacks.

---

# Why the Unified Kill Chain Matters

Modern cyber attacks are rarely linear.

Attackers often:

- Gain an initial foothold.
- Escalate privileges.
- Move laterally across the network.
- Maintain persistence.
- Repeat these activities until they reach their objective.

The Unified Kill Chain models this behaviour more accurately than the traditional Cyber Kill Chain.

---

# The Three Major Phases

## Initial Foothold

The attacker gains initial access to the target environment.

Examples include:

- Phishing emails
- Exploiting public-facing applications
- Compromised credentials
- Supply chain attacks

### Defensive Focus

- Email security
- Multi-Factor Authentication (MFA)
- Vulnerability management
- Web Application Firewalls (WAF)

---

## Network Propagation

After gaining access, the attacker expands control within the environment.

Common activities include:

- Privilege escalation
- Credential dumping
- Lateral movement
- Discovery
- Persistence

This stage often repeats multiple times as the attacker moves through the network.

### Defensive Focus

- Endpoint Detection and Response (EDR)
- Active Directory monitoring
- Network segmentation
- Privileged Access Management (PAM)
- Continuous monitoring

---

## Action on Objectives

The attacker completes their mission.

Examples include:

- Data exfiltration
- Ransomware deployment
- Service disruption
- Financial fraud
- Destruction of systems

### Defensive Focus

- Data Loss Prevention (DLP)
- Incident Response
- Backup and Recovery
- Security monitoring

---

# Cyber Kill Chain vs Unified Kill Chain

| Cyber Kill Chain | Unified Kill Chain |
|------------------|--------------------|
| Linear attack model | Multi-stage attack model |
| Seven attack phases | Expanded attack lifecycle |
| Focus on initial intrusion | Focus on the entire intrusion |
| Limited coverage of lateral movement | Extensive coverage of lateral movement and persistence |

The Unified Kill Chain provides a more realistic representation of how attackers operate in modern enterprise environments.

---

# Real-World Example

An attacker sends a phishing email to an employee.

After the employee opens the attachment:

1. The attacker gains initial access.
2. Privileges are escalated.
3. Credentials are stolen.
4. Additional systems are compromised.
5. Sensitive file servers are discovered.
6. Data is collected.
7. Information is exfiltrated.
8. Ransomware is deployed.

Instead of ending after the first compromise, the attacker repeatedly moves through the environment until the objective is achieved.

---

# Practical Skills Developed

During this room I learned:

- Understanding modern attack lifecycles.
- Recognizing attacker progression.
- Understanding persistence.
- Understanding lateral movement.
- Thinking about enterprise-wide incident response.

---

# Key Terminology

| Term | Description |
|------|-------------|
| Initial Foothold | The attacker's first successful access to a target environment. |
| Lateral Movement | Moving from one compromised system to another within a network. |
| Privilege Escalation | Gaining higher-level permissions after initial access. |
| Persistence | Maintaining long-term access to a compromised system. |
| Data Exfiltration | Unauthorized transfer of sensitive information out of an organization. |

---

# Interview Questions

## What is the Unified Kill Chain?

The Unified Kill Chain is a framework that models the complete lifecycle of modern cyber attacks, combining concepts from the Cyber Kill Chain and MITRE ATT&CK to better represent attacker behaviour.

---

## Why was the Unified Kill Chain created?

It was created because modern attacks often involve repeated stages such as lateral movement and persistence, which are not fully represented by the traditional Cyber Kill Chain.

---

## What is lateral movement?

Lateral movement is the process of moving from one compromised system to another after gaining initial access, allowing attackers to expand their control within a network.

---

## Why is the Unified Kill Chain useful for SOC analysts?

It helps analysts understand how attackers progress through an environment, making it easier to detect suspicious behaviour, investigate incidents, and disrupt attacks before attackers reach their objectives.

---

# Connections to My Home Lab

The Unified Kill Chain relates closely to my home lab environment.

Examples include:

- Windows Server and Active Directory for authentication and privilege management.
- pfSense firewall logs for monitoring network communication.
- Windows and Ubuntu virtual machines for understanding attacker movement between systems.
- Future SIEM deployments to correlate events across different stages of an attack.

As I continue developing my lab, I plan to simulate different stages of the attack lifecycle to better understand how each phase can be detected and investigated.

---

# Key Takeaways

- Modern attacks are rarely linear.
- Attackers often repeat stages such as discovery, privilege escalation, and lateral movement.
- The Unified Kill Chain provides a more realistic model of enterprise attacks.
- Defenders have multiple opportunities to detect and disrupt attacker activity.

---

# Personal Reflection

Before completing this room, I viewed attacks mainly through the traditional Cyber Kill Chain.

After learning the Unified Kill Chain, I understand that attackers frequently move through an environment over an extended period rather than following a single, fixed sequence of steps. This framework has helped me appreciate the importance of continuous monitoring, endpoint visibility, and understanding attacker behaviour throughout the entire attack lifecycle.
