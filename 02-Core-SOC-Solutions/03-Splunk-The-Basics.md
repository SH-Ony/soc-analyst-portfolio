# Splunk: The Basics

## Overview

Splunk is one of the most widely used Security Information and Event Management (SIEM) platforms in modern Security Operations Centers (SOCs). It collects, indexes, searches, and visualizes machine-generated data, allowing analysts to investigate security events and detect suspicious activity.

This room introduced the basic concepts of Splunk and demonstrated how security analysts search and investigate logs using Splunk's Search Processing Language (SPL).

---

# Learning Objectives

After completing this room, I can:

- Understand the purpose of Splunk in a SOC.
- Explain how Splunk collects and stores log data.
- Perform basic searches using Search Processing Language (SPL).
- Filter and investigate security events.
- Understand dashboards, indexes, and alerts.

---

# Why Splunk is Important

Modern organizations generate millions of events every day.

Splunk allows SOC analysts to:

- Centralize log collection
- Search massive amounts of data quickly
- Investigate suspicious activity
- Create dashboards
- Build alerts
- Support incident response

Without tools like Splunk, investigating enterprise environments would be extremely difficult.

---

# How Splunk Works

A simplified Splunk workflow:

1. Devices generate logs.
2. Splunk Forwarders collect the logs.
3. Logs are sent to the Splunk Indexer.
4. Events are indexed and stored.
5. Analysts search the data using SPL.
6. Dashboards and alerts help identify suspicious activity.

---

# Core Components

## Splunk Forwarder

Collects logs from endpoints and forwards them to Splunk.

Examples:

- Windows Server
- Linux Server
- Firewall
- Active Directory

---

## Indexer

Processes, indexes, and stores incoming data so it can be searched efficiently.

---

## Search Head

Provides the web interface used by analysts.

Typical tasks include:

- Searching logs
- Building dashboards
- Investigating alerts
- Creating reports

---

# Search Processing Language (SPL)

Splunk uses its own query language called **Search Processing Language (SPL)**.

Basic searches include:

```spl
index=main
```

Search for Windows Event ID:

```spl
EventCode=4625
```

Search failed logins:

```spl
EventCode=4625 Account_Name=*
```

Filter by host:

```spl
host=WIN-SERVER
```

Search by source IP:

```spl
src=192.168.1.10
```

---

# Common Investigation Workflow

1. Receive a SIEM alert.
2. Open Splunk.
3. Search related logs.
4. Identify affected hosts.
5. Review timestamps.
6. Investigate user activity.
7. Build an event timeline.
8. Document findings.

---

# Dashboards

Dashboards provide a visual overview of security events.

Examples include:

- Failed login attempts
- Malware detections
- Authentication activity
- VPN connections
- Firewall events

Dashboards help analysts quickly identify abnormal activity.

---

# Alerts

Splunk can automatically generate alerts when predefined conditions are met.

Examples:

- Multiple failed logins
- PowerShell execution
- Malware detection
- Privileged account activity
- Impossible travel

---

# Real-World Example

An employee reports that their computer is behaving unusually.

A SOC analyst opens Splunk and searches:

- Windows Event Logs
- Authentication events
- Process creation logs
- Network connections

The analyst identifies suspicious PowerShell activity followed by communication with an external IP address.

The investigation is documented and escalated for further response.

---

# Skills Practiced

During this room I learned:

- Basic Splunk navigation
- SPL fundamentals
- Searching logs
- Filtering events
- Investigating security alerts
- Understanding dashboards

---

# Key Terminology

| Term | Description |
|------|-------------|
| SPL | Search Processing Language used by Splunk. |
| Index | A repository where Splunk stores searchable data. |
| Forwarder | Software that sends logs to Splunk. |
| Indexer | Stores and indexes incoming log data. |
| Search Head | Web interface used for searching and investigations. |
| Dashboard | Visual representation of log data and security events. |

---

# Interview Questions

## What is Splunk?

Splunk is a SIEM platform that collects, indexes, searches, and visualizes machine-generated data to support security monitoring and investigations.

---

## What is SPL?

SPL (Search Processing Language) is Splunk's query language used to search, filter, and analyze log data.

---

## Why do SOC analysts use Splunk?

Splunk allows analysts to quickly search large amounts of log data, investigate incidents, correlate events, and monitor security activity through dashboards and alerts.

---

## What is an Index?

An Index is the location where Splunk stores searchable log data.

---

# Connections to My Home Lab

This room connects well with my enterprise home lab.

Current connections include:

- Windows Server generating Event Logs.
- Active Directory authentication events.
- pfSense firewall logs.
- Windows and Ubuntu virtual machines.

As I continue expanding my lab, I plan to integrate centralized log collection to practice searching and investigating events using concepts learned from Splunk.

---

# Key Takeaways

- Splunk is one of the most widely used SIEM platforms.
- SPL enables analysts to efficiently search and investigate security events.
- Dashboards and alerts improve visibility into enterprise environments.
- Splunk plays a central role in SOC investigations and incident response.

---

# Personal Reflection

Before completing this room, I viewed Splunk simply as a log viewer.

After completing it, I understand that Splunk is a powerful investigation platform that enables SOC analysts to collect, search, correlate, and visualize security events across an organization's infrastructure.

Learning the basics of SPL also showed me how effective searching is essential for investigating alerts and building incident timelines.
