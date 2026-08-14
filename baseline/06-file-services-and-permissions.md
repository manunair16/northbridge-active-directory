# 📂 File Services & Permissions

## 🎯 Objective

Configure and document Windows file-sharing and access permissions for the NorthBridge environment.

The baseline uses both **share permissions** and **NTFS permissions** to control access to shared resources.

---

## 📁 File Sharing

Department-based resources were configured as Windows file shares to represent organizational file access requirements.

The baseline includes access controls associated with groups such as:

* `GG_Finance`
* `GG_IT`

Access is managed through security groups rather than assigning permissions individually to every user.

---

## 🔐 Share Permissions

Share-level permissions were configured to control access to the shared resource over the network.

The configured security groups provide the basis for determining which users can access the shared resource.

---

## 🛡️ NTFS Permissions

NTFS permissions were configured on the underlying folders to provide file-system-level access control.

This creates a second permission layer that must be considered when troubleshooting access.

The effective access available to a user depends on the combination of:

```text id="x8m2qp"
👤 User
   ↓
👥 Security Group Membership
   ↓
📤 Share Permissions
   ↓
📁 NTFS Permissions
   ↓
🔐 Effective Access
```

---

## 📸 Evidence

| Evidence                   | What it demonstrates                      |
| -------------------------- | ----------------------------------------- |
| `1. share permissions.png` | 📤 Share-level permission configuration   |
| `2. ntfs permissions.png`  | 🛡️ NTFS permissions on the shared folder |

---

## 🔍 Validation

The permission configuration was reviewed to confirm:

* ✅ Share permissions are configured for the intended security groups.
* ✅ NTFS permissions are configured on the underlying folder.
* ✅ Security groups are used as the primary access-control mechanism.
* ✅ Share and NTFS permissions can be evaluated independently during troubleshooting.

The resulting configuration provides the known-good permission baseline for subsequent access-control scenarios.

---

## 💡 Key Takeaway

Windows file access can involve multiple layers of permissions.

When a user reports that they cannot access a shared resource, troubleshooting should therefore consider:

1. 👤 User identity
2. 👥 Security group membership
3. 📤 Share permissions
4. 🛡️ NTFS permissions
5. 🔐 Effective access

This baseline will be used as the reference configuration for **Case 1 – Finance Folder Access Issue**.
