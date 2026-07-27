# Windows Reconnaissance Detection using Sysmon & Splunk

## Project Overview

This project demonstrates how to detect Windows reconnaissance activity using Sysmon and Splunk Enterprise in a SOC lab environment.

The objective is to simulate attacker discovery commands, collect telemetry from Sysmon, create real-time detection rules in Splunk, generate alerts, and investigate the resulting events.

This project follows the workflow used by Security Operations Centers (SOCs) for endpoint monitoring and threat detection.

---

## Objectives

- Build a Windows endpoint monitoring lab
- Collect process creation events using Sysmon
- Ingest Sysmon logs into Splunk Enterprise
- Detect reconnaissance commands using SPL
- Configure real-time alerts
- Investigate the generated events
- Map detections to the MITRE ATT&CK framework

---

## Technologies Used

- Windows 10
- VMware Workstation
- Sysmon
- SwiftOnSecurity Sysmon Configuration
- Splunk Enterprise
- SPL (Search Processing Language)

---

## Lab Architecture

*Architecture diagram will be added here.*

---

## Detection Workflow

1. Simulate reconnaissance commands
2. Sysmon records process creation events
3. Windows Event Logs store telemetry
4. Splunk ingests Sysmon logs
5. SPL detection identifies reconnaissance activity
6. Splunk generates an alert
7. SOC analyst investigates the event

---

## MITRE ATT&CK Mapping

| Technique | ID |
|----------|----|
| System Owner/User Discovery | T1033 |
| System Information Discovery | T1082 |
| Account Discovery | T1087 |
| Network Configuration Discovery | T1016 |

---

## Repository Structure

```
windows-reconnaissance-detection-sysmon-splunk/
├── README.md
├── detections/
├── reports/
├── screenshots/
├── architecture/
├── LICENSE
└── .gitignore
```

---

## Status

✅ Project 1 Complete – Windows Reconnaissance Detection