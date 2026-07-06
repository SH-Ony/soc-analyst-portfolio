# Pyramid of Pain

## Overview

The Pyramid of Pain is a defensive security model created by David Bianco. It ranks different Indicators of Compromise (IOCs) based on how difficult they are for an attacker to change after being detected.

The higher an indicator appears in the pyramid, the more disruptive it is for an attacker when defenders detect and block it.

Rather than focusing only on simple indicators such as IP addresses or file hashes, defenders should prioritize detections that force attackers to modify their tools, techniques, or procedures.

---

# Learning Objectives

After completing this room, I can:

- Explain the purpose of the Pyramid of Pain.
- Describe each level of the pyramid.
- Understand why higher-level detections are more valuable.
- Relate the Pyramid of Pain to threat detection and incident response.

---

# Why the Pyramid of Pain Matters

Not all Indicators of Compromise provide the same defensive value.

Blocking a malicious IP address may temporarily stop an attack, but an attacker can easily use a different IP.

However, detecting an attacker's tactics or techniques forces them to redesign parts of their attack, making future attacks more difficult and expensive.

The Pyramid of Pain helps SOC analysts prioritize detections that have the greatest defensive impact.

---

# Levels of the Pyramid

## 1. Hash Values

Examples:

- MD5
- SHA1
- SHA256

Hashes uniquely identify files.

### Advantages

- Easy to detect.
- Useful for known malware.

### Limitations

Attackers can modify a file slightly, generating a completely new hash.

Pain for attacker:

⭐ Very Low

---

## 2. IP Addresses

Examples:

- Command and Control (C2) servers
- Malicious hosts

### Advantages

- Easy to block.
- Useful during investigations.

### Limitations

Attackers can quickly switch to different servers or cloud infrastructure.

Pain for attacker:

⭐⭐ Low

---

## 3. Domain Names

Examples:

- Phishing domains
- Malware download domains

### Advantages

- Can identify malicious infrastructure.

### Limitations

Attackers frequently register new domains.

Pain for attacker:

⭐⭐⭐ Moderate

---

## 4. Network / Host Artifacts

Examples:

- Registry keys
- File paths
- User-Agent strings
- Scheduled tasks
- Named pipes

These artifacts are left behind during attacker activity.

Pain for attacker:

⭐⭐⭐⭐ Significant

---

## 5. Tools

Examples:

- Mimikatz
- PsExec
- Cobalt Strike
- Metasploit

Rather than detecting infrastructure, defenders identify the tools attackers rely on.

Changing tools requires additional effort and testing.

Pain for attacker:

⭐⭐⭐⭐⭐ High

---

## 6. Tactics, Techniques and Procedures (TTPs)

Examples:

- Credential dumping
- Lateral movement
- Privilege escalation
- PowerShell abuse
- Pass-the-Hash

This is the highest level of the pyramid.

Instead of detecting a specific tool, defenders detect the attacker's behaviour.

Changing behaviour often requires redesigning the entire attack.

Pain for attacker:

⭐⭐⭐⭐⭐⭐ Very High

---

# Pyramid Summary

| Level | Difficulty for Attacker |
|---------|-----------------------|
| Hashes | Very Low |
| IP Addresses | Low |
| Domains | Moderate |
| Network / Host Artifacts | Significant |
| Tools | High |
| TTPs | Very High |

As defenders move higher in the pyramid, detections become more valuable because they force attackers to invest more time and resources.

---

# Real-World Example

A SOC analyst detects a malicious IP address communicating with a workstation.

Blocking the IP prevents communication, but the attacker simply switches to another server.

Later, the analyst creates a detection rule for PowerShell downloading remote content.

Even if the attacker changes the IP address or domain, the behaviour is still detected.

The second detection is far more valuable because it targets the attacker's technique rather than a single indicator.

---

# Practical Skills Developed

During this room I learned:

- Understanding different Indicators of Compromise (IOCs)
- Prioritizing defensive detections
- Thinking from a defender's perspective
- Understanding attacker adaptability
- Identifying higher-value detection opportunities

---

# Key Terminology

| Term | Description |
|------|-------------|
| IOC | Indicator of Compromise used to identify malicious activity. |
| Hash | A unique fingerprint of a file. |
| Artifact | Evidence left behind by attacker activity. |
| TTP | Tactics, Techniques, and Procedures used by attackers. |
| Detection Rule | Logic used to identify suspicious activity. |

---

# Interview Questions

## What is the Pyramid of Pain?

The Pyramid of Pain is a framework that ranks indicators based on how difficult they are for attackers to change after defenders detect them.

---

## Why are TTPs at the top of the pyramid?

Because changing attacker behaviour requires significantly more effort than changing simple indicators such as IP addresses or file hashes.

---

## Which level provides the greatest defensive value?

Tactics, Techniques, and Procedures (TTPs), because they target attacker behaviour rather than easily replaceable indicators.

---

## Why shouldn't defenders rely only on IP addresses?

IP addresses can be changed quickly, making them less effective as long-term detection methods.

---

# Connections to My Home Lab

This room relates closely to the monitoring and logging concepts I am developing in my home lab.

Examples include:

- Windows Event Logs capturing attacker behaviour.
- PowerShell logging.
- Active Directory authentication events.
- pfSense firewall logs.
- Future SIEM detection rules based on attacker techniques instead of individual indicators.

As I continue expanding my home lab, I plan to build detections that focus on attacker behaviour rather than only blocking individual indicators.

---

# Key Takeaways

- Not all IOCs provide equal defensive value.
- Higher-level detections are more difficult for attackers to bypass.
- Detecting behaviour is more effective than detecting infrastructure.
- The Pyramid of Pain helps SOC analysts prioritize stronger detections.

---

# Personal Reflection

Before completing this room, I mainly viewed Indicators of Compromise as individual pieces of evidence such as IP addresses or file hashes.

After completing it, I now understand that the most effective detections focus on attacker behaviour. This room reinforced the importance of building detections that force adversaries to change their techniques rather than simply replacing infrastructure.
