# Investigation Report – Windows Reconnaissance Detection

## Incident Summary

A series of Windows reconnaissance commands were executed on the monitored endpoint. Sysmon captured the process creation events, which were successfully ingested into Splunk Enterprise. A real-time detection rule identified the activity and generated an alert for investigation.

---

## Alert Information

**Alert Name:** Windows Reconnaissance Detection

**Severity:** Medium

**Data Source:** Sysmon Event ID 1 (Process Creation)

---

## Attack Simulation

The following commands were executed during the simulation:

```cmd
whoami
hostname
ipconfig /all
net user
net localgroup administrators
systeminfo
```

---

## Detection Logic

The Splunk detection rule searched for process creation events involving common reconnaissance utilities.

Targeted executables:

- whoami.exe
- hostname.exe
- ipconfig.exe
- net.exe
- systeminfo.exe

---

## Investigation Findings

The investigation confirmed:

- Sysmon successfully logged each process creation event.
- Splunk indexed the events correctly.
- The detection rule matched the simulated reconnaissance commands.
- A real-time alert was generated.
- Parent process information was available for investigation.

Observed fields included:

- Time
- Computer
- User
- ParentImage
- Image
- CommandLine

---

## MITRE ATT&CK Mapping

| Technique | ID |
|-----------|----|
| System Owner/User Discovery | T1033 |
| System Information Discovery | T1082 |
| Account Discovery | T1087 |
| Network Configuration Discovery | T1016 |

---

## Outcome

The simulated reconnaissance activity was successfully detected and investigated using Sysmon and Splunk Enterprise. This demonstrates the effectiveness of endpoint telemetry and SIEM-based detection for identifying post-compromise discovery techniques.