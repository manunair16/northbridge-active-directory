# 🏢 NorthBridge AD Baseline v1.0

## 📌 Purpose

This directory documents the known-good baseline configuration of the NorthBridge Active Directory environment.

The baseline was established before beginning scenario-based troubleshooting exercises.

---

## 🖥️ Environment

| Component             | Details               |
| --------------------- | --------------------- |
| 🌐 Domain             | `northbridge.local`   |
| 🖥️ Domain Controller | `SRV-DC01`            |
| 💻 Client             | `FIN-PC01`             |
| 🪟 Server OS          | Windows Server 2025   |
| 🪟 Client OS          | Windows 11        |
| 📦 Virtualization     | VirtualBox |

---

## 🔧 Baseline Components

The baseline includes:

* 🖥️ Domain Controller
* 🏢 Active Directory
* 🌐 DNS
* 🗂️ Organizational Units
* 👤 Domain Users
* 👥 Security Groups
* ⚙️ Group Policy
* 🔐 Password Policy
* 📂 File Services
* 📤 Share Permissions
* 🛡️ NTFS Permissions
* 🔗 Client Domain Join
* 🔑 Domain Authentication

---

## 📸 Evidence

Detailed configuration evidence is organized by technical area:

| Area                           | Documentation                                                                  |
| ------------------------------ | ------------------------------------------------------------------------------ |
| 🖥️ Domain Controller          | [`01-domain-controller.md`](./01-domain-controller.md)                         |
| 🏢 Active Directory            | [`02-active-directory.md`](./02-active-directory.md)                           |
| 🌐 DNS                         | [`03-dns.md`](./03-dns.md)                                                     |
| 👥 Users & Groups              | [`04-users-and-groups.md`](./04-users-and-groups.md)                           |
| ⚙️ Group Policy                | [`05-group-policy.md`](./05-group-policy.md)                                   |
| 📂 File Services & Permissions | [`06-file-services-and-permissions.md`](./06-file-services-and-permissions.md) |
| 💻 Client Domain Join          | [`07-client-domain-join.md`](./07-client-domain-join.md)                       |

Supporting screenshots are available under:

`evidence/`

---

## ✅ Baseline Validation

The environment was functionally validated by confirming:

* ✅ Active Directory is available.
* ✅ DNS is configured for the domain.
* ✅ Users and security groups are configured.
* ✅ Group Policy and password policy are configured.
* ✅ File-sharing and NTFS permissions are configured.
* ✅ `FIN-PC01` successfully joined `northbridge.local`.
* ✅ Domain authentication was successfully tested from the client.

---

## 🎯 Baseline Status

**NorthBridge AD Baseline v1.0 — Established**

This baseline represents the known-good state used as the reference point for subsequent troubleshooting and scenario-based investigations.

