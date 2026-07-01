
# SOC Alert Triage

## Objective

Alert triage is the process of reviewing security alerts, determining their legitimacy, assessing their severity, and deciding the appropriate response.

The goal is to identify genuine security incidents while minimizing the time spent on false positives.

---

## Typical Alert Triage Workflow

1. Receive alert
2. Validate the alert
3. Collect contextual information
4. Determine severity
5. Decide whether it is:

- False Positive
- Benign Activity
- True Positive

6. Escalate or close the case

---

## Information Collected

- Source IP
- Destination IP
- Username
- Hostname
- Timestamp
- Event Type
- Process Name
- Parent Process
- File Hash
- Network Connections

---

## Severity Levels

### Low

Minor event with little security impact.

Example:

- Single failed login
- Antivirus informational alert

---

### Medium

Suspicious activity requiring investigation.

Example:

- Multiple failed logins
- Unusual PowerShell execution

---

### High

Confirmed malicious behavior requiring immediate action.

Example:

- Ransomware detected
- Credential dumping
- Malware execution

---

## Key Lesson

Alert triage is a decision-making process rather than simply reviewing alerts. The objective is to efficiently distinguish between normal activity and genuine security incidents while minimizing analyst fatigue.
