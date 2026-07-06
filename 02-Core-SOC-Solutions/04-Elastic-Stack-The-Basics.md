
# Elastic Stack: The Basics

## Overview

The Elastic Stack (commonly known as ELK) is a collection of tools used to collect, process, search, and visualize large volumes of log data. It is widely used in Security Operations Centers (SOCs) for security monitoring, threat detection, and incident investigations.

The Elastic Stack consists of four main components:

- Elasticsearch
- Logstash
- Kibana
- Beats

Together, these components provide centralized log management and powerful search capabilities for security analysts.

---

# Learning Objectives

After completing this room, I can:

- Explain the purpose of the Elastic Stack.
- Identify the role of each Elastic component.
- Understand how logs flow through the Elastic Stack.
- Explain how Kibana is used during investigations.
- Understand how Elastic supports SOC monitoring.

---

# Why the Elastic Stack is Important

Modern enterprise environments generate logs from thousands of devices.

The Elastic Stack helps organizations:

- Collect logs from many sources
- Process and normalize data
- Store searchable information
- Visualize security events
- Investigate suspicious activity
- Support threat hunting

---

# Components of the Elastic Stack

## Elasticsearch

Elasticsearch is the search engine of the Elastic Stack.

Responsibilities:

- Store indexed log data
- Fast searching
- Data aggregation
- Event correlation

---

## Logstash

Logstash processes incoming log data before it reaches Elasticsearch.

Responsibilities:

- Collect logs
- Parse different log formats
- Transform data
- Forward processed events

---

## Kibana

Kibana provides the graphical interface used by analysts.

SOC analysts use Kibana to:

- Search logs
- Build dashboards
- Visualize events
- Investigate incidents
- Create reports

---

## Beats

Beats are lightweight agents installed on endpoints.

Examples include:

- Winlogbeat
- Filebeat
- Auditbeat
- Packetbeat
- Metricbeat

Their purpose is to collect specific types of data and forward them into the Elastic Stack.

---

# How Logs Flow

A simplified Elastic workflow:

```
Endpoints / Servers
        │
        ▼
      Beats
        │
        ▼
    Logstash
        │
        ▼
 Elasticsearch
        │
        ▼
     Kibana
        │
        ▼
  SOC Analyst
```

---

# Investigation Workflow

A typical SOC investigation using Elastic:

1. Security event occurs.
2. Beats collect logs.
3. Logstash processes the data.
4. Elasticsearch indexes the events.
5. Kibana displays dashboards.
6. Analysts search logs.
7. Suspicious activity is investigated.

---

# Kibana Dashboards

Dashboards provide analysts with an overview of:

- Authentication activity
- Firewall events
- Endpoint activity
- Network traffic
- Security alerts
- System health

Dashboards help identify unusual behavior quickly.

---

# Real-World Example

A Windows workstation begins making connections to an unusual external IP address.

The Elastic Stack collects:

- Windows Event Logs
- Network connections
- DNS requests
- Firewall logs

Using Kibana, the analyst searches for the endpoint, reviews the timeline, and correlates events from multiple log sources to determine whether the activity is malicious.

---

# Skills Practiced

During this room I learned:

- Elastic Stack architecture
- Elasticsearch fundamentals
- Kibana navigation
- Log collection concepts
- Basic investigation workflow
- Security monitoring fundamentals

---

# Key Terminology

| Term | Description |
|------|-------------|
| Elasticsearch | Search and indexing engine used to store and query log data. |
| Logstash | Processes and transforms incoming log data. |
| Kibana | Web interface used for visualization and investigations. |
| Beats | Lightweight agents that collect data from endpoints. |
| Index | Searchable collection of stored log data. |

---

# Interview Questions

## What is the Elastic Stack?

The Elastic Stack is a collection of tools used to collect, process, store, search, and visualize log data for monitoring and security investigations.

---

## What are the four main components?

- Elasticsearch
- Logstash
- Kibana
- Beats

---

## What is Kibana used for?

Kibana provides dashboards and visualization tools that help analysts search logs, investigate alerts, and monitor security events.

---

## What is the role of Beats?

Beats are lightweight data collection agents that gather logs or system information from endpoints and forward them into the Elastic Stack.

---

# Connections to My Home Lab

The Elastic Stack relates directly to my personal cybersecurity home lab.

Current connections include:

- Windows Server Event Logs
- Active Directory authentication events
- pfSense firewall logs
- Windows and Ubuntu virtual machines

As my home lab develops, I plan to deploy centralized logging to gain practical experience with Elastic-based monitoring and investigations.

---

# Key Takeaways

- The Elastic Stack provides centralized log management.
- Elasticsearch enables fast searching and indexing.
- Kibana is used for dashboards and investigations.
- Beats collect data from endpoints.
- Elastic is widely used for security monitoring in SOC environments.

---

# Personal Reflection

Before completing this room, I only knew that the Elastic Stack was another SIEM solution.

After completing it, I now understand how each component contributes to collecting, processing, storing, and visualizing security data. I also have a better understanding of how analysts use Kibana to investigate events and monitor enterprise environments.
