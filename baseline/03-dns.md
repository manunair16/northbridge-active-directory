# 🌐 DNS Configuration

## 🎯 Objective

Configure and validate DNS services required for the **NorthBridge Active Directory environment**.

DNS is a critical part of Active Directory because domain clients need to locate and communicate with domain services such as the domain controller.

---

## ⚙️ Configuration

DNS was configured on the domain controller:

`SRV-DC01`

The Active Directory domain is:

`northbridge.local`

The DNS configuration provides name resolution for the domain and supports communication between the domain controller and joined Windows clients.

---

## 📸 Evidence

| Evidence             | What it demonstrates                                         |
| -------------------- | ------------------------------------------------------------ |
| `1. dns manager.png` | 🌐 DNS Manager and the `northbridge.local` DNS configuration |

---

## 🔍 What Was Verified

The DNS configuration was reviewed to confirm:

* ✅ The DNS service is available on `SRV-DC01`.
* ✅ The `northbridge.local` DNS zone is present.
* ✅ DNS is integrated with the Active Directory environment.
* ✅ The configuration provides the name-resolution foundation required for domain operations.

---

## 🧪 Functional Validation

DNS functionality was further validated during the Windows client domain-join process.

The client:

`FIN-PC01`

was successfully joined to:

`northbridge.local`

This provides practical validation that the client could locate and communicate with the domain environment.

The domain-join evidence is documented separately under the client domain-join section.

---

## 💡 Key Takeaway

DNS is not treated as a separate service from Active Directory in this environment.

It provides an important dependency for:

* 🔎 Domain service discovery
* 💻 Client-to-domain-controller communication
* 🔐 Domain authentication
* 🏢 Active Directory operations
* 🌐 Windows client domain joining
* 🔍 Troubleshooting domain connectivity

Understanding this relationship will also be important in later DNS and domain-connectivity troubleshooting scenarios.

