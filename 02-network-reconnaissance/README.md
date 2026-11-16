
# 02 - Network Reconnaissance and SMB Investigation

## Overview

This section documents network connectivity testing, service discovery and SMB file-sharing investigations conducted within the SOC home lab.

The exercise used Kali Linux as the testing machine and Windows 11 as the target endpoint. Both virtual machines communicated through NAT networking in a controlled environment.

## Lab Environment

| Component | Configuration |
|---|---|
| Testing machine | Kali Linux |
| Target machine | Windows 11 |
| Network mode | NAT |
| Windows IP | 192.168.40.128 |
| Kali Linux IP | 192.168.40.129 |
| SMB service | TCP 445 |

## Activities Completed

### 1. Network Connectivity Testing

- Configured communication between Kali Linux and Windows 11.
- Tested network connectivity using ping.
- Identified and resolved an initial connectivity issue.
- Verified communication between both virtual machines.

### 2. Windows File Sharing Configuration

- Enabled Network Discovery.
- Enabled File and Printer Sharing.
- Created a shared folder named Labshare.
- Configured sharing permissions.
- Used netstat to verify SMB was listening on TCP port 445.

### 3. SMB Connectivity and Enumeration

From Kali Linux:

- Used nc to test TCP port 445.
- Used Nmap to validate SMB port availability.
- Used smbclient to authenticate to the Windows shared folder.
- Accessed the Labshare directory.
- Downloaded test.txt.
- Verified the downloaded file contents: "SOC Portfolio lab".

### 4. Nmap Service and Version Discovery

Performed an Nmap service/version scan against the Windows virtual machine.

The following open ports were identified:

| Port | Status |
|---|---|
| 135 | Open |
| 139 | Open |
| 445 | Open |
| 5357 | Open |

SMB information was also reviewed as part of the investigation.

### 5. Sysmon Event Investigation

Reviewed the Sysmon Operational log following network reconnaissance.

Events investigated:

| Event ID | Description | Observation |
|---|---|---|
| 1 | Process Creation | Multiple events observed |
| 3 | Network Connection | Not observed under initial configuration |
| 22 | DNS Query | One event observed |

The process taskhostw.exe was investigated and identified as legitimate within the lab context.

## Analyst Observations

- SMB was reachable from Kali Linux over TCP port 445.
- Windows file sharing was successfully accessed.
- Nmap identified four open ports on the Windows endpoint.
- Sysmon generated process creation and DNS query telemetry.
- Network testing and endpoint event analysis were correlated.

## Skills Demonstrated

- NAT networking and virtual machine connectivity.
- Network troubleshooting.
- Nmap service and port discovery.
- TCP connectivity testing using nc.
- Windows SMB configuration.
- SMB enumeration using smbclient.
- Windows network administration.
- Sysmon event investigation.
- Security event correlation.

## Evidence

Supporting screenshots and investigation evidence will be stored in the evidence directory.

## Project Information

**Project:** Enterprise SOC Home Lab  
**Platform:** VMware Workstation Pro  
**Testing OS:** Kali Linux  
**Target OS:** Windows 11  
**Author:** Temitope Akande
