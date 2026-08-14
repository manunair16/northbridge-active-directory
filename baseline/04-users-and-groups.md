# 👥 Users & Security Groups

## 🎯 Objective

Configure domain users and security groups in Active Directory to establish a structured approach to **identity and access management** within the NorthBridge environment.

The configuration provides the foundation for assigning access through group membership rather than managing permissions individually for every user.

---

## 👤 Domain Users

Domain user accounts were created within the `northbridge.local` Active Directory environment.

These accounts are used throughout the lab to represent users who require access to organizational resources.

User accounts provide the identity used for:

* 🔐 Domain authentication
* 📂 Resource access
* 👥 Security group membership
* 🧪 Scenario-based testing

---

## 👥 Security Groups

Security groups were created to represent access requirements within the environment.

Examples include department-oriented groups such as:

* `GG_Finance`
* `GG_IT`

Using security groups provides a more manageable way to assign resource access.

Instead of assigning permissions directly to individual users, access can be associated with the appropriate group and users can then be managed through group membership.

---

## 🔐 Group Membership

Users were added to the appropriate security groups based on their intended role or department.

This establishes the relationship between:

```text
👤 User
   ↓
👥 Security Group
   ↓
🔐 Resource Access
```

The actual resource permissions are documented separately under the file-services and permissions section.

---

## 📸 Evidence

| Evidence                  | What it demonstrates                                |
| ------------------------- | --------------------------------------------------- |
| `1. domain users.png`     | 👤 Domain user accounts in Active Directory         |
| `2. security groups.png`  | 👥 Security groups configured for access management |
| `3. group membership.png` | 🔐 Users assigned to security groups                |

---

## ✅ Validation

The configuration was validated by confirming:

* ✅ Domain user accounts are present in Active Directory.
* ✅ Required security groups are available.
* ✅ Users can be assigned to the appropriate groups.
* ✅ Group membership can be used as the basis for resource access.
* ✅ The configuration can be used for subsequent permission and access-control testing.

---

## 💡 Key Takeaway

Security groups provide a structured method for managing access in an Active Directory environment.

This approach becomes particularly important when troubleshooting access issues because user identity, group membership, share permissions, and NTFS permissions can be examined separately to determine where an access failure occurs.

The next baseline section documents the **Group Policy configuration**, followed by file-sharing and permission controls.
