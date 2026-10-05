# SOC + Honeynet (Live Traffic) in Azure
<img src="https://github.com/DivineFotabi/SOC-Honeynet-Live-Traffic-in-Azure/blob/4fd162e762a2e41d31af61c4208b2de40ca084c6/Azure%20Diagram%202.png" />

# Objective
In this project, I build a mini honeynet in Azure and ingest logs from various resources into a Log Analytics Workspace. Using Microsoft Sentinel as my SIEM, I was able to query the security logs, monitor live attacks, trigger alerts and create incidents. I measured some security metrics in the insecure environment for 24 hours, applied security controls to harden the environment, measured metrics for another 24 hours. The goal is to detect, investigate, and mitigate real-world cyber threats using Microsoft Sentinel and Defender for Cloud.

# Skills Learned

- Deploying Microsoft Sentinel as a SIEM for log collection and threat detection.
- Implementing Defender for Cloud for compliance enforcement.
- Monitoring Windows security logs and Entra ID logs for threat detection.
- Simulating a Windows brute-force attack followed by post-exploitation activities.
- Investigating the attack telemetry and correlating evidence using Sentinel logs.
- Comparing pre- and post-hardening security effectiveness.

# Tools

- Microsoft Sentinel – SIEM for log analysis & correlation.
- Microsoft Defender for Cloud – Compliance & security monitoring.
- Log Analytics Workspace.
- Windows Security Logs
- Linux Event Logs.
- Azure key vault.
- Azure Entra ID Logs.
- SecurityIncident (Incidents created by Sentinel)

# Setup
- Deployed Windows victim VMs in Azure for monitoring.
- Deployed linux victim VMs in Azure for monitoring.
- Configured NSG rules to log and monitor external connections.
- Configured Azure Key Vault for Monitoring.
- Configure Azure Microsoft Sentinel.
- Configure Azure Microsoft storage account.
- Enabled log forwarding for:
  - Windows Security Logs (Failed logins, logon attempts, privilege escalation).
  - Entra ID Logs (Authentication tracking, MFA violations).
  - Microsoft Defender Incident.
  - Defender for Cloud Security Alerts (Policy compliance monitoring).
  - Integrated all logs into Microsoft Sentinel for correlation

Windows Events Logs
<img src="https://github.com/DivineFotabi/SOC-Honeynet-Live-Traffic-in-Azure/blob/bbf394430cb9cfa85cd2a9cd9c9055596d0f62b8/KQL%201.png" />

Linux syslogs
<img src="https://github.com/DivineFotabi/SOC-Honeynet-Live-Traffic-in-Azure/blob/994c35f98b3a7e55ccda1c11378f4e1eb2e7b165/Syslogs%201.png" />

SiginLogs
<img src="https://github.com/DivineFotabi/SOC-Honeynet-Live-Traffic-in-Azure/blob/10d3484d8d6ef08cfd61912959010a1fe4660e57/S.%20LOGS.png" />

Brute Force & Privelliage Escallation
- Kali Linux executed an RDP brute-force attack against a Windows VM.
- Sentinel generated an alert for multiple failed login attempts (Event ID 4625).
- Successful login achieved using brute force, triggering an alert in Defender for Cloud.

<img src="https://github.com/DivineFotabi/SOC-Honeynet-Live-Traffic-in-Azure/blob/466e39054d9cdd14610465081f46518d988e63c6/Brute%20F%20and%20possibly%20Escallation.png" />

Incident Response
<img src="https://github.com/DivineFotabi/SOC-Honeynet-Live-Traffic-in-Azure/blob/f5dde6d8f8b15697954e6c2c7705e22473b7a26d/Incident%20Response.png" />

MITRE ATT&CK
<img src="https://github.com/DivineFotabi/SOC-Honeynet-Live-Traffic-in-Azure/blob/e76ca4fc3590739ca4a22d4438a98354128574be/Mitre%20Attack%20ss.png" />

World location
<img src="https://github.com/DivineFotabi/SOC-Honeynet-Live-Traffic-in-Azure/blob/39244910410e3694ea8e1b434552eae0f008c4b6/workbook%201.png" /> 

Linux syslogs
<img src="https://github.com/DivineFotabi/SOC-Honeynet-Live-Traffic-in-Azure/blob/8dd4d78860efcdebe161195e2848cca549f2f21e/Syslogs%202.png" />

Microsoft Defender
<img src="https://github.com/DivineFotabi/SOC-Honeynet-Live-Traffic-in-Azure/blob/785348e83c738bbc4df1b3255636f9c7ae7e58fa/Microsoft%20Denfender.png" />

# Security Controls
The following data shows the metric I measured in the insecured environment for 48hours

SecurityEvents = 165951 

Syslogs        =18126  

Security Alerts = 48    

Security Incident = 40  

# Conclusion

- Successfully built an Azure-based SOC & Honeynet for real-world attack detection.
- Integrated log sources into a Log Analytics workspace and configured Microsoft Sentinel for threat detection and incident management.
- Simulated a Windows brute-force attack and investigated the incident using Sentinel logs.
- Utilized Microsoft Defender Threat Intelligence (MDTI) to enrich threat investigations.
- Measured security metrics
- Continuous monitoring is essential, as legitimate user activity could generate additional security events, requiring ongoing refinement of detection rules and response strategies.
