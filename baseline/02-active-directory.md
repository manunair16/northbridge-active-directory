# 🏢 Active Directory Structure

## 🎯 Objective

Configure and organize the **NorthBridge Active Directory domain** to provide a structured foundation for managing users, groups, computers, and access within the environment.

---

## 🌐 Domain

The Active Directory environment is based on:

`northbridge.local`

The domain is managed through **Active Directory Users and Computers (ADUC)** on the domain controller:

`SRV-DC01`

---

## 🗂️ Organizational Structure

Organizational Units (OUs) were created to provide logical separation of directory objects.

The OU structure helps with:

* 👥 User administration
* 💻 Computer management
* 🔐 Group Policy targeting
* 🛡️ Access management
* 🧭 Easier administration and troubleshooting

The OU structure is also used as a foundation for the scenario-based exercises that follow.

---

## 📸 Evidence

| Evidence                        | What it demonstrates                                                       |
| ------------------------------- | -------------------------------------------------------------------------- |
| `1. active directory users and computers.png` | 🏢 Active Directory Users and Computers and the `northbridge.local` domain |
| `2. ou structure.png`           | 🗂️ Organizational Unit structure within the domain                        |

---

## ✅ Validation

The Active Directory structure was validated by confirming:

* ✅ The `northbridge.local` domain is available in ADUC.
* ✅ The expected Organizational Units are present.
* ✅ Directory objects can be managed through the Active Directory management interface.
* ✅ The OU structure provides a logical foundation for user, computer, and Group Policy administration.

---

## 💡 Key Takeaway

A structured Active Directory design makes it easier to manage **users, computers, policies, and access** as the environment grows.

The OU structure established here provides the organizational foundation for the user-management, Group Policy, permissions, and troubleshooting activities documented later in this project.
