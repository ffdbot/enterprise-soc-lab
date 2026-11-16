
# SOC Analyst Portfolio | Enterprise SOC Lab

**Author:** Temitope Akande  
**Project:** Enterprise Security Operations Centre (SOC) Home Lab  
**Environment:** VMware Workstation | Windows 11 | Kali Linux | Azure | Microsoft Sentinel

---

## Project Overview

This repository documents my practical cybersecurity learning journey through the design, deployment and investigation activities carried out in an enterprise-style Security Operations Centre (SOC) home lab.

The project focuses on endpoint monitoring, security event analysis, network reconnaissance, cloud monitoring and Security Information and Event Management (SIEM).

The lab was built using VMware Workstation, Windows 11, Kali Linux, Microsoft Sysinternals, Sysmon, Azure Log Analytics and Microsoft Sentinel.

## Lab Architecture

The lab environment consists of:

- **Host:** Windows 11 laptop running VMware Workstation Pro.
- **Windows Endpoint:** Windows 11 virtual machine used for security monitoring and investigation.
- **Linux Environment:** Kali Linux virtual machine used for controlled network testing and reconnaissance.
- **Endpoint Monitoring:** Microsoft Sysinternals and Sysmon.
- **Cloud Infrastructure:** Microsoft Azure.
- **Log Management:** Azure Log Analytics Workspace.
- **SIEM:** Microsoft Sentinel.
- **Query Language:** Kusto Query Language (KQL).

### Monitoring Workflow

Windows Endpoint → Azure Monitor Agent → Log Analytics Workspace → Microsoft Sentinel → KQL Investigation → Security Analysis

## Technical Skills Demonstrated

| Area | Technologies / Skills |
|---|---|
| Virtualisation | VMware Workstation |
| Operating Systems | Windows 11, Kali Linux |
| Networking | NAT, SMB, Nmap, Ping, Netstat |
| Windows Administration | PowerShell, Command Prompt |
| Endpoint Monitoring | Sysmon, Sysinternals |
| Event Analysis | Windows Event Viewer |
| Cloud Security | Microsoft Azure |
| SIEM | Microsoft Sentinel |
| Log Management | Azure Log Analytics, Azure Monitor |
| Security Queries | KQL |
| Investigation | Event correlation and troubleshooting |

## Practical Investigations

### 1. Virtualisation and Endpoint Deployment
- Deployed Windows 11 and Kali Linux virtual machines.
- Configured virtual machine resources and networking.
- Installed VMware Tools and created recovery snapshots.
- Installed Sysinternals and Sysmon.

### 2. Network Reconnaissance
- Established connectivity between Kali Linux and Windows.
- Configured and tested SMB file sharing.
- Used Nmap to identify exposed services and open ports.
- Investigated network connectivity and service availability.

### 3. Windows Endpoint Monitoring
- Performed Windows host enumeration using CMD and PowerShell.
- Generated controlled endpoint activity.
- Reviewed process creation telemetry.
- Investigated Sysmon Event ID 1.

### 4. Sysmon Security Investigations

| Event ID | Investigation |
|---|---|
| 1 | Process Creation |
| 3 | Network Connection |
| 11 | File Creation |
| 13 | Registry Value Set |

Investigations included examining process metadata, network activity, file creation and registry modifications.

### 5. Azure Cloud SIEM Deployment
- Created an Azure resource group.
- Deployed a Log Analytics Workspace.
- Enabled Microsoft Sentinel.
- Configured Azure Monitor and a Data Collection Rule.
- Associated the Data Collection Rule with the monitored virtual machine.
- Configured budget alerts and managed cloud resource costs.

### 6. Microsoft Sentinel Investigation

**Investigation: Windows Failed Logon Attempts**

- Investigated Windows Security Event ID 4625.
- Checked endpoint availability and Azure Monitor Agent communication.
- Verified security event generation in Windows Event Viewer.
- Queried the SecurityEvent table in Microsoft Sentinel.
- Identified returned failed-logon records using KQL.

## Evidence and Documentation

The repository includes a consolidated technical journal containing investigation notes, screenshots, configurations, troubleshooting activities and lessons learned.

**[View the Complete SOC Analyst Portfolio Journal (PDF)](SOC_Analyst_Portfolio_Master_Journal_FINAL.pdf)**

## Troubleshooting and Lessons Learned

Throughout the project, I documented and resolved practical challenges involving:

- VMware virtual machine compatibility.
- Kali Linux mouse and display issues.
- Network connectivity between virtual machines.
- Sysmon event filtering and configuration.
- Azure Monitor Agent communication.
- Missing security event ingestion.
- Azure resource and cost management.

These exercises strengthened my troubleshooting, analytical thinking and technical documentation skills.

## Evidence Integrity

This repository distinguishes between activities supported by direct screenshots and those documented through written investigation records.

The recovered evidence directly supports the investigations described in the portfolio. Where screenshots or complete query text were unavailable, this is identified rather than presented as verified evidence.

## Future Development

Planned improvements include:

- Additional Microsoft Sentinel KQL investigations.
- Security incident investigation and reporting.
- Threat hunting exercises.
- Detection engineering.
- Microsoft Defender XDR integration.
- Security automation using Python.

---

**This portfolio represents practical, hands-on cybersecurity development and continuous learning towards a career in Security Operations and Cybersecurity.**

