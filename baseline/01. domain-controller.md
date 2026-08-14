# 🖥️ Domain Controller Configuration

## 🎯 Objective

Establish the Windows Server foundation for the **NorthBridge Active Directory environment** and prepare the server to operate as the primary domain controller.

---

## 🧰 Environment

| Component           | Details                                 |
| ------------------- | --------------------------------------- |
| 🖥️ Server          | `SRV-DC01`                              |
| 🪟 Operating System | Windows Server 2025 Standard Evaluation |
| 🌐 Domain           | `northbridge.local`                     |
| 📦 Virtualization   | VirtualBox                              |

---

## ⚙️ Configuration

### 1️⃣ Server Identity

The Windows Server instance was renamed to:

`SRV-DC01`

This server is used as the primary domain controller for the NorthBridge Active Directory environment.

### 2️⃣ 🌐 Network Configuration

The server was configured with a static IPv4 address and the required network settings.

The network configuration was established before validating the Active Directory environment to provide consistent connectivity and DNS services for the domain.

### 3️⃣ 🧩 Server Roles

The required Windows Server roles and services were configured to support the NorthBridge environment, including:

* 🔐 Active Directory Domain Services (AD DS)
* 🌐 DNS
* 📂 File and Storage Services

The server was subsequently configured to support the:

`northbridge.local`

Active Directory domain.

---

## 📸 Evidence

| Evidence                       | What it demonstrates                               |
| ------------------------------ | -------------------------------------------------- |
| `1. server identity.png`       | 🖥️ Server hostname and Windows Server environment |
| `2. network configuration.png` | 🌐 Server network configuration                    |
| `3. server manager roles.png`  | 🧩 Installed Windows Server roles and services     |

---

## ✅ Validation

The configuration was validated by confirming:

* ✅ The server is identified as `SRV-DC01`.
* ✅ The required network configuration is present.
* ✅ Active Directory Domain Services is available.
* ✅ DNS is available for the environment.
* ✅ The server provides the foundation for the `northbridge.local` domain.
* ✅ A Windows client was subsequently able to join the domain.

Client domain-join and authentication validation are documented separately in the baseline evidence.

---

## 💡 Key Takeaway

This configuration establishes the **server-side foundation** for the NorthBridge Active Directory environment.

It provides the infrastructure required for:

* 🔐 Centralized identity management
* 🌐 DNS-based domain services
* 👤 Domain authentication
* ⚙️ Group Policy
* 🔒 Access-control management
* 🔍 Subsequent troubleshooting and security scenarios

