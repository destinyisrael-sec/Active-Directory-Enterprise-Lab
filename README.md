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
 
  - ## Active Directory Configuration

### Domain Controller

- Hostname: DC01
- Operating System: Windows Server 2022
- Domain: lab.local
- DNS: Active Directory-integrated DNS

### Organizational Units

The following organizational units were created to organize users and security groups:

- IT
- Security

### IT Users

- Alex Smith
- James Wilson

### Security Groups

- IT-Admins
- IT-Users

- ## Group Policy Configuration

A Domain Password Security GPO was created and linked to the IT organizational unit.

Password policy configuration:

- Enforce password history: 5 passwords remembered
- Maximum password age: 90 days
- Minimum password age: 1 day
- Minimum password length: 12 characters
- Password complexity requirements: Enabled

The policy was successfully applied to the Windows 11 domain-joined workstation.

## Domain Authentication Testing

A Windows 11 workstation was successfully joined to the lab.local Active Directory domain.

Domain authentication was tested using the Alex Smith domain account.

Successful authentication confirmed:

- Windows 11 domain membership
- Active Directory user authentication
- Communication between the workstation and Domain Controller

- ## Security Event Testing

A controlled failed authentication was performed using a dedicated AD test account.

Windows Security generated:

- Event ID: 4625
- Account: ad.test
- Failure reason: Unknown user name or bad password

This demonstrates how failed authentication attempts are recorded by Windows and provides a foundation for SIEM-based detection.

## Evidence

### Domain User Authentication

![Domain User Login](screenshots/ad-domain-user-login.png)

### Windows 11 Domain Membership

![Windows 11 Domain Membership](screenshots/ad-windows11-domain-membership.png)

### Group Policy Applied

![Domain Password Security GPO](screenshots/ad-gpo-applied.png)

### Failed Domain Authentication

![Windows Event ID 4625](screenshots/ad-domain-user-failed-logon-4625.png)

### Network

- VirtualBox Host-Only Network
- Domain Controller: 192.168.56.10
- Windows 11 Client: 192.168.56.20

## Status

Status

🟢 Core Active Directory Lab Completed
🟡 Wazuh SIEM Integration In Progress
