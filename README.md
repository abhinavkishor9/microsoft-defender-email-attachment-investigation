# microsoft-defender-email-attachment-investigation
## Overview

This lab demonstrates how Microsoft Defender detects and quarantines a malicious email attachment using the EICAR antivirus test file.

The objective was to simulate a user opening a suspicious email attachment and investigate the complete detection lifecycle using Windows Defender Operational logs.

---

## Lab Objectives

- Simulate a malicious email attachment
- Trigger Microsoft Defender real-time protection
- Investigate Defender Operational logs
- Analyze malware detection details
- Verify quarantine action
- Document findings from a SOC analyst perspective

---

## Lab Environment

- Windows 10
- Microsoft Defender Antivirus
- Windows Event Viewer
- PowerShell
- VMware Workstation
- EICAR Test File

---

## Attack Simulation

1. Created a working directory

```
C:\EmailLab
```

2. Downloaded the EICAR antivirus test file.

3. Opened the attachment to simulate a user executing an email attachment.

4. Microsoft Defender detected the file immediately.

5. Defender quarantined the file automatically.

6. Investigated Windows Defender Operational logs.

7. Reviewed Windows Security Protection History.

8. Verified that the malicious file had been removed.

---

## Evidence Collected

- Defender Operational Event ID 1117
- Protection History
- Malware detection details
- Quarantine action
- File path
- Detection source
- Detection severity
- Cleanup verification

---

## Key Findings

Microsoft Defender successfully detected the EICAR test malware using Real-Time Protection and immediately quarantined the file before execution could continue.

The investigation confirmed:

- Malware name
- File location
- Detection source
- Process involved
- Detection severity
- Automatic remediation

---

## Skills Demonstrated

- Microsoft Defender Investigation
- Malware Detection
- Windows Event Analysis
- SOC Alert Triage
- Endpoint Security Monitoring
- Incident Documentation
- Threat Validation

---

## MITRE ATT&CK Mapping

| Tactic | Technique |
|---------|-----------|
| Initial Access | T1566.001 – Phishing Attachment |
| Execution | T1204.002 – User Execution |
| Defense Evasion | Prevented by Microsoft Defender |

---

## Outcome

The simulated malicious attachment was detected, quarantined, investigated, and documented successfully without impacting the system.
