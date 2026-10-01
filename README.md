# SOC + Honeynet (Live Traffic) in Azure
<img src="https://github.com/DivineFotabi/SOC-Honeynet-Live-Traffic-in-Azure/blob/4712b40c0e7143a704c49e206bdcdd4f7f0cdafe/Azure%20Diagram1.png" />

# Objective
In this project, I build a mini honeynet in Azure and ingest logs from various resources into a Log Analytics Workspace. Using Microsoft Sentinel as my SIEM, I was able to query the security logs, monitor live attacks, trigger alerts and create incidents. I measured some security metrics in the insecure environment for 24 hours, applied security controls to harden the environment, measured metrics for another 24 hours. The goal is to detect, investigate, and mitigate real-world cyber threats using Microsoft Sentinel and Defender for Cloud.

# Skills Learned

Deploying Microsoft Sentinel as a SIEM for log collection and threat detection.
Implementing Defender for Cloud for compliance enforcement.
Monitoring Windows security logs and Entra ID logs for threat detection.
Simulating a Windows brute-force attack followed by post-exploitation activities.
Investigating the attack telemetry and correlating evidence using Sentinel logs.
Comparing pre- and post-hardening security effectiveness.

# Tools

Microsoft Sentinel – SIEM for log analysis & correlation.
Microsoft Defender for Cloud – Compliance & security monitoring.
Log Analytics Workspace.
Windows Security Logs
Linux Event Logs.
Azure Entra ID Logs.
SecurityIncident (Incidents created by Sentinel)
