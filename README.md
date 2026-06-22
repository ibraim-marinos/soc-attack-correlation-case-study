# Multi-Stage Attack Investigation

## Overview

This project documents a simulated SOC investigation where Windows authentication logs and PowerShell telemetry were correlated to reconstruct a potential attack chain.

The investigation identified:

- Multiple failed login attempts (Event ID 4625)
- Successful authentication activity (Event ID 4624)
- PowerShell execution and file download activity (Event ID 4104)
- Timeline reconstruction
- MITRE ATT&CK mapping

---

## Investigation Workflow

### Phase 1 – Authentication Analysis

Multiple failed authentication attempts were identified within a short timeframe.

Evidence suggested potential credential access activity.

### Phase 2 – Authentication Validation

Successful authentication events were observed after repeated failures.

This increased confidence that valid credentials may have been obtained.

### Phase 3 – PowerShell Activity Analysis

PowerShell Event ID 4104 revealed Invoke-WebRequest activity used to download a file.

This suggested post-compromise execution behavior.

---

## Skills Demonstrated

- Incident Response
- Log Analysis
- Event Correlation
- Timeline Reconstruction
- Threat Detection
- MITRE ATT&CK Mapping
- Security Reporting

---

## MITRE ATT&CK

- T1110 – Brute Force
- T1078 – Valid Accounts
- T1059.001 – PowerShell
- T1105 – Ingress Tool Transfer

---

## Full Investigation Report

📄 Download Full Investigation Report
