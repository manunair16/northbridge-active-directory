# 💻 Client Domain Join & Authentication

## 🎯 Objective

Join a Windows client to the **NorthBridge Active Directory domain** and validate successful domain authentication.

This provides functional validation that the server, DNS, Active Directory, and client configuration work together.

---

## 🖥️ Client Environment

| Component             | Details             |
| --------------------- | ------------------- |
| 💻 Client             | `FIN-PC01`           |
| 🪟 Operating System   | Windows 11      |
| 🌐 Domain             | `northbridge.local` |
| 🖥️ Domain Controller | `SRV-DC01`          |
| 📦 Virtualization     | VirtualBox        |

---

## 🔗 Domain Join

The Windows client `FIN-PC01` was successfully joined to:

`northbridge.local`

The successful domain join demonstrates that the client was able to locate and communicate with the Active Directory environment.

---

## 🔐 Domain Authentication

Following the domain join, a domain account was used to authenticate successfully on the Windows client.

This provides functional evidence that the client can communicate with the domain environment and perform domain authentication.

---

## 📸 Evidence

| Evidence                         | What it demonstrates                                    |
| -------------------------------- | ------------------------------------------------------- |
| `1. client domain join.png`      | 🔗 `FIN-PC01` successfully joined to `northbridge.local` |
| `2. domain login validation.png` | 🔐 Successful domain authentication on the client       |

---

## 🔍 Validation

The following were successfully validated:

* ✅ Client `FIN-PC01` is joined to `northbridge.local`.
* ✅ The client can communicate with the domain environment.
* ✅ Domain authentication succeeds from the client.
* ✅ The Active Directory environment is operational from the client perspective.

This provides functional validation of the relationship between the Windows client, DNS, Active Directory, and domain controller.

---

## 💡 Key Takeaway

The domain join and authentication tests provide an end-to-end validation of the NorthBridge environment.

The baseline now demonstrates the complete path from:

```text
🖥️ Domain Controller
        ↓
🌐 DNS
        ↓
🏢 Active Directory
        ↓
💻 Windows Client
        ↓
🔗 Domain Join
        ↓
🔐 Domain Authentication
```

This known-good state will be used as the starting point for the scenario-based troubleshooting exercises.
