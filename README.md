# NorthBridge Enterprise Active Directory

![Windows Server](https://img.shields.io/badge/Windows%20Server-2025-0078D4?logo=windows\&logoColor=white)
![Active Directory](https://img.shields.io/badge/Active%20Directory-AD%20DS-0078D4?logo=microsoft\&logoColor=white)
![DNS](https://img.shields.io/badge/DNS-Configured-4285F4)
![Group Policy](https://img.shields.io/badge/Group%20Policy-Configured-5C2D91)
![VirtualBox](https://img.shields.io/badge/VirtualBox-Lab-183A61?logo=virtualbox\&logoColor=white)
![UTM](https://img.shields.io/badge/UTM-Lab-000000)

## 📌 Project Overview

NorthBridge is a hands-on Windows Active Directory lab built to practice and demonstrate real-world **IT administration, identity and access management, troubleshooting, and security operations** skills.

The environment includes a Windows Server domain controller and a Windows client joined to the domain. The project starts with a known-good Active Directory baseline and then uses realistic support and security scenarios to demonstrate **investigation, troubleshooting, remediation, and validation**.

This repository documents **my own implementation, screenshots, findings, and troubleshooting work**.

---

## 🖥️ Lab Environment

| Component             | Details               |
| --------------------- | --------------------- |
| 🌐 Domain             | `northbridge.local`   |
| 🖥️ Domain Controller | `SRV-DC01`            |
| 💻 Client             | `IT-PC01` `FIN-PC01` `HR-PC01` `OPS-PC01` `MGT-PC01`|
| 🪟 Server OS          | Windows Server 2025   |
| 🪟 Client OS          | Windows 11           |
| 📦 Virtualization     | VirtualBox            |

---

## 🛠️ Technologies & Skills

### Windows Administration

* Windows Server
* Windows 11
* Active Directory Domain Services (AD DS)
* DNS
* Windows File Services
* Windows Client Administration

### Identity & Access Management

* User Management
* Security Groups
* Group Membership
* Organizational Units (OUs)
* Domain Authentication
* NTFS Permissions
* Share Permissions
* Access Control

### Troubleshooting & Security

* Access and Permission Issues
* Authentication Issues
* DNS and Domain Connectivity
* Group Policy
* Windows Client Troubleshooting
* Root-Cause Analysis
* Evidence Collection
* Security Investigation
* Incident Handling
* Technical Documentation

---

## 🏗️ What I Built

### Active Directory Baseline

The baseline environment includes:

* Windows Server domain controller
* `northbridge.local` Active Directory domain
* DNS configuration
* Organizational Units
* Domain users
* Security groups
* Group memberships
* Group Policy
* Password policy
* Department file shares
* NTFS permissions
* Share permissions
* Windows client domain joining
* Domain authentication

The baseline acts as the **known-good environment** for the troubleshooting cases that follow.

---

## 🔎 Scenario-Based Troubleshooting

After establishing the baseline, I work through realistic IT and security scenarios.

Examples include:

* 📁 Finance folder access problems
* 🔐 Incorrect or missing permissions
* 👤 User account and access issues
* 🔑 Authentication problems
* ⚙️ Group Policy issues
* 🌐 DNS and domain connectivity problems
* 💻 Windows client troubleshooting
* 🛡️ Security investigations
* 🚨 Incident handling

Each case follows a simple investigation process:

```text
Problem
   ↓
Investigation
   ↓
Evidence Collection
   ↓
Root Cause
   ↓
Resolution
   ↓
Validation
   ↓
Documentation
```

This demonstrates not only configuration skills, but also the ability to **investigate and resolve problems systematically**.

---

## 🤝 Collaboration

This is an **individual project with collaborative scenario work**.

Three participants — **[Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk), [Mr. Manu P Nair](https://github.com/manunair16) and [Mr. Varun M Nair](https://github.com/varunmnair95)** — maintain their own independent lab environments and GitHub repositories.

The physical/lab environments are not shared. Collaboration takes place mainly during scenario-based cases through:

* Troubleshooting discussions
* Sharing investigation approaches
* Comparing findings
* Role-based case activities
* Problem-solving
* Technical communication

Each repository represents the individual's **own implementation, screenshots, findings, and documentation**.

---

## 📸 Evidence & Documentation

Screenshots and technical evidence are included throughout the repository to show the actual work performed.

Evidence covers areas such as:

* 🖥️ Server configuration
* 🌐 Network configuration
* 🏢 Active Directory
* 🌐 DNS
* 👥 Users and groups
* ⚙️ Group Policy
* 📂 File and folder permissions
* 💻 Client domain joining
* 🔍 Troubleshooting results

Screenshots are supported by short explanations describing:

**What was done → Why it was done → What the evidence shows → How it was validated**

---

## 📂 Repository Structure

```text
northbridge-active-directory/
│
├── README.md
│
├── baseline/
│   ├── README.md
│   └── evidence/
│
├── cases/
│   ├── README.md
│   └── case-01-finance-folder-access/
│
├── documentation/
│   ├── troubleshooting/
│   ├── change-management/
│   └── lessons-learned/
│
└── diagrams/
```

---

## 🎯 Skills Demonstrated

| Area                       | Skills                                                                         |
| -------------------------- | ------------------------------------------------------------------------------ |
| 🖥️ Windows Administration | Windows Server, Windows 11, AD DS, DNS, File Services                          |
| 👤 Identity & Access       | Users, Groups, OUs, Authentication, NTFS & Share Permissions                   |
| 🔍 Troubleshooting         | Access Issues, Authentication, DNS, Group Policy, Client Administration        |
| 🛡️ Security Operations    | Evidence Collection, Investigation, Incident Handling, Access-Control Analysis |
| 📝 Documentation           | Findings, Validation, Troubleshooting Records, Lessons Learned                 |

---

## 📊 Project Status

**Active Directory Baseline:** ✅ Completed

**Scenario-Based Cases:** 🔄 In Progress

The project will continue to expand with additional **troubleshooting, administration, and security scenarios**.

---

## ⚠️ Disclaimer

This is an isolated lab environment created for **learning, practice, and portfolio development**.

No production systems or real organizational data are involved.
