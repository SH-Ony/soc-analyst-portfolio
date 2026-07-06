# Introduction to Security Orchestration, Automation and Response (SOAR)

## Overview

Security Orchestration, Automation, and Response (SOAR) is a technology designed to help Security Operations Centers (SOCs) automate repetitive security tasks, coordinate multiple security tools, and improve incident response efficiency.

Instead of manually performing repetitive actions for every alert, SOAR platforms use predefined workflows (playbooks) to automate routine tasks, allowing analysts to focus on more complex investigations.

---

# Learning Objectives

After completing this room, I can:

- Explain the purpose of SOAR.
- Understand the difference between orchestration and automation.
- Describe how playbooks are used in incident response.
- Explain how SOAR improves SOC efficiency.
- Understand where SOAR fits within a modern SOC.

---

# Why SOAR is Important

Security teams often receive hundreds or even thousands of alerts every day.

Without automation:

- Analysts spend significant time performing repetitive tasks.
- Response times increase.
- Human error becomes more likely.
- Alert fatigue affects analyst performance.

SOAR helps reduce these challenges by automating repetitive investigation and response activities.

---

# What Does SOAR Mean?

## Security

Integrates security tools used within the organization.

Examples include:

- SIEM
- EDR
- Firewalls
- Threat Intelligence Platforms
- Email Security Solutions
- Ticketing Systems

---

## Orchestration

Orchestration connects multiple security tools so they work together during an investigation.

Example:

A SIEM generates an alert.

↓

SOAR automatically queries the EDR platform.

↓

The firewall is checked.

↓

Threat intelligence is queried.

↓

Results are collected for the analyst.

---

## Automation

Automation performs predefined actions without requiring manual intervention.

Examples include:

- Enriching alerts
- Collecting Indicators of Compromise (IOCs)
- Looking up IP reputation
- Creating incident tickets
- Sending notifications
- Blocking malicious IP addresses
- Isolating compromised endpoints

---

## Response

Once enough information has been gathered, SOAR assists analysts by executing predefined response actions or providing recommendations.

---

# Playbooks

Playbooks are predefined workflows that guide automated investigations and responses.

Example phishing playbook:

1. Receive phishing alert.
2. Extract URLs.
3. Check URL reputation.
4. Scan attachments.
5. Query threat intelligence.
6. Create investigation ticket.
7. Notify analyst.
8. Escalate if malicious.

Playbooks ensure investigations are performed consistently and efficiently.

---

# Typical SOAR Workflow

```
Security Alert
       │
       ▼
    SIEM Alert
       │
       ▼
SOAR Playbook Starts
       │
       ▼
Threat Intelligence Lookup
       │
       ▼
Query EDR
       │
       ▼
Check Firewall Logs
       │
       ▼
Create Ticket
       │
       ▼
Notify Analyst
```

---

# Benefits of SOAR

- Reduces repetitive manual work.
- Improves incident response speed.
- Reduces analyst fatigue.
- Standardizes investigations.
- Improves collaboration.
- Allows analysts to focus on higher-priority incidents.

---

# Limitations

SOAR is not a replacement for SOC analysts.

Challenges include:

- Poorly designed playbooks can automate incorrect actions.
- Human judgment is still required for complex investigations.
- Playbooks require regular maintenance.
- Automation depends on accurate integrations between security tools.

---

# Real-World Example

A user receives a phishing email.

The SIEM detects suspicious email activity.

SOAR automatically:

- Extracts URLs from the email.
- Checks URL reputation.
- Queries VirusTotal.
- Searches for similar emails.
- Creates an incident ticket.
- Sends results to the SOC analyst.

Instead of performing each step manually, the analyst receives enriched information and can quickly determine whether further action is required.

---

# Skills Practiced

During this room I learned:

- SOAR fundamentals.
- Security orchestration concepts.
- Security automation.
- Playbook design.
- Automated incident response workflows.

---

# Key Terminology

| Term | Description |
|------|-------------|
| SOAR | Security Orchestration, Automation, and Response platform. |
| Orchestration | Coordinating multiple security tools during an investigation. |
| Automation | Performing predefined actions automatically. |
| Playbook | A predefined workflow for investigating or responding to security incidents. |
| IOC | Indicator of Compromise such as malicious IPs, domains, or file hashes. |
| Enrichment | Automatically gathering additional context about an alert. |

---

# Interview Questions

## What is SOAR?

SOAR is a security platform that integrates multiple security tools and automates repetitive investigation and response tasks using predefined playbooks.

---

## What is the difference between SIEM and SOAR?

A SIEM collects, correlates, and analyzes security logs to detect suspicious activity.

SOAR automates investigation and response actions after alerts are generated.

SIEM detects.

SOAR automates.

---

## What is a playbook?

A playbook is a predefined sequence of investigation or response actions that can be executed automatically or with analyst approval.

---

## Does SOAR replace SOC analysts?

No.

SOAR automates repetitive tasks but still relies on analysts to investigate complex incidents, make decisions, and respond appropriately.

---

# Connections to My Home Lab

Although I have not yet deployed a SOAR platform in my home lab, this room helped me understand how automation fits into a modern SOC.

As my home lab grows, I plan to integrate additional security tools and explore how automated workflows can simplify alert investigation and incident response.

---

# Key Takeaways

- SOAR automates repetitive security tasks.
- Orchestration connects multiple security tools.
- Playbooks standardize investigations.
- Automation improves SOC efficiency.
- Human analysts remain essential for decision-making.

---

# Personal Reflection

Before completing this room, I thought SOAR was simply another security tool.

After completing it, I now understand that SOAR acts as the automation layer within a Security Operations Center. It connects multiple security technologies, enriches alerts with additional context, and automates repetitive workflows, allowing analysts to spend more time on complex investigations and incident response.
