
# Introduction to Endpoint Detection and Response (EDR)

## Overview

Endpoint Detection and Response (EDR) is a security technology designed to continuously monitor endpoint devices such as workstations, laptops, and servers. Unlike traditional antivirus software, EDR focuses on detecting suspicious behaviour, collecting endpoint telemetry, and assisting analysts during investigations.

EDR provides visibility into endpoint activity and enables Security Operations Center (SOC) analysts to investigate, contain, and respond to threats.

---

# Learning Objectives

After completing this room, I can:

- Explain the purpose of EDR.
- Understand how EDR differs from traditional antivirus.
- Identify common endpoint telemetry collected by EDR.
- Understand how analysts investigate endpoint alerts.
- Describe common EDR response actions.

---

# Why EDR is Important

Endpoints are one of the most common targets for attackers.

Examples include:

- Phishing malware
- Ransomware
- Credential theft
- Malicious PowerShell execution
- Remote access trojans (RATs)

EDR helps organizations detect these attacks early by monitoring endpoint behaviour in real time.

---

# How EDR Works

A typical EDR workflow:

1. An endpoint continuously generates activity.
2. The EDR agent monitors the endpoint.
3. Suspicious behaviour is detected.
4. Alerts are generated.
5. Analysts investigate the activity.
6. If necessary, the endpoint can be isolated to prevent further compromise.

---

# Common EDR Capabilities

- Process monitoring
- File monitoring
- Registry monitoring
- Network connection monitoring
- Command-line visibility
- Threat detection
- Endpoint isolation
- Investigation timeline

---

# EDR vs Antivirus

| Traditional Antivirus | EDR |
|-----------------------|-----|
| Signature-based detection | Behaviour-based detection |
| Detects known malware | Detects suspicious behaviour |
| Limited investigation capability | Rich investigation timeline |
| Limited response | Endpoint isolation and response actions |

---

# Real-World Example

A user downloads a malicious attachment from a phishing email.

The endpoint begins running PowerShell commands to download additional malware.

The EDR agent detects the abnormal PowerShell activity, generates an alert, records the process tree, and allows the SOC analyst to investigate the full execution chain.

If confirmed malicious, the analyst can isolate the endpoint to stop lateral movement.

---

# Skills Practiced

- Understanding endpoint telemetry
- Understanding behavioural detection
- Endpoint investigation concepts
- Security monitoring fundamentals

---

# Key Terminology

| Term | Description |
|------|-------------|
| Endpoint | A device connected to a network, such as a laptop or server. |
| Telemetry | Security-related data collected from an endpoint. |
| Process Tree | Parent-child relationship between running processes. |
| Isolation | Disconnecting an endpoint from the network while keeping it available for investigation. |

---

# Interview Questions

## What is EDR?

EDR is a security solution that continuously monitors endpoint devices, collects telemetry, detects suspicious behaviour, and helps analysts investigate and respond to threats.

---

## How is EDR different from antivirus?

Traditional antivirus primarily detects known malware using signatures, whereas EDR continuously monitors endpoint behaviour and supports investigation and response.

---

## Why is endpoint telemetry important?

Telemetry provides analysts with the evidence needed to reconstruct attacker activity and understand how a compromise occurred.

---

# Personal Reflection

Before this room, I viewed EDR mainly as an advanced antivirus solution.

After completing the room, I now understand that EDR provides continuous endpoint visibility, investigation capabilities, and response actions that are essential for modern Security Operations Centers.
