# MITRE ATT&CK Mapping

| Stage | Technique | MITRE ID |
|-------|-----------|-----------|
| 1 | Brute Force | T1110 |
| 2 | Valid Accounts | T1078 |
| 3 | Command and Scripting Interpreter: PowerShell | T1059.001 |
| 3 | Ingress Tool Transfer | T1105 |

## Summary

The attack chain was reconstructed through authentication logs and PowerShell telemetry.

The findings were mapped to MITRE ATT&CK to better understand attacker behavior and attack progression.

### Attack Progression

1. **Brute Force (T1110)**  
   Multiple failed authentication attempts were observed against the target endpoint.

2. **Valid Accounts (T1078)**  
   A successful authentication event occurred following repeated login failures.

3. **PowerShell Execution (T1059.001)**  
   PowerShell Event ID 4104 revealed script execution activity using Invoke-WebRequest.

4. **Ingress Tool Transfer (T1105)**  
   The PowerShell command was used to download a file from an external source.

This sequence suggests a multi-stage attack involving credential access, successful authentication, and post-compromise activity.
