# Active Directory Enterprise Lab

## Project Overview

This project demonstrates the deployment of an enterprise Active Directory environment using Windows Server 2022, Windows 11, VirtualBox and Wazuh SIEM.

## Technologies

- Windows Server 2022
- Active Directory Domain Services
- DNS
- Group Policy
- Windows 11
- Ubuntu Linux
- Wazuh SIEM
- VirtualBox

## Objectives

- Build an Active Directory Domain Controller
- Join Windows clients to the domain
- Configure Organizational Units (OUs)
- Create users and groups
- Apply Group Policy Objects (GPOs)
- Monitor domain events using Wazuh
- Simulate attacks for threat detection

- ## Lab Architecture

The lab consists of a Windows Server 2022 Domain Controller, a domain-joined Windows 11 workstation, and an Ubuntu/Wazuh SIEM environment.

### Environment

- DC01 — Windows Server 2022
  - Active Directory Domain Services
  - DNS
  - Group Policy
  - Domain: lab.local

- Windows 11 Client
  - Domain joined to lab.local
  - Domain user authentication
  - Windows Security Event monitoring

- Ubuntu Linux
  - Wazuh Manager
  - SIEM monitoring
  - Security event analysis

### Network

- VirtualBox Host-Only Network
- Domain Controller: 192.168.56.10
- Windows 11 Client: 192.168.56.20

## Status

Status

🟢 Core Active Directory Lab Completed
🟡 Wazuh SIEM Integration In Progress
