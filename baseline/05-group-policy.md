# ⚙️ Group Policy & Password Policy

## 🎯 Objective

Configure and document Group Policy settings used to establish a consistent security baseline for the NorthBridge Active Directory environment.

Group Policy provides centralized control over Windows configuration and security settings across domain-joined systems.

---

## ⚙️ Group Policy Configuration

Group Policy was configured within the `northbridge.local` Active Directory environment.

The policy configuration provides a centralized method for managing security-related settings rather than configuring each workstation independently.

The baseline includes account and password-related settings that can be applied to domain users and systems.

---

## 🔐 Password Policy

The password policy was configured with the following settings:

| Setting                    | Configuration |
| -------------------------- | ------------: |
| 🔑 Minimum password length |  8 characters |
| ⏱️ Minimum password age    |       30 days |
| 📅 Maximum password age    |       90 days |
| 🛡️ Password complexity    |   Not Defined |

> **Note:** Password complexity is documented as **Not Defined** based on the captured configuration evidence. No claim of complexity enforcement is made.

---

## 📸 Evidence

| Evidence                 | What it demonstrates                               |
| ------------------------ | -------------------------------------------------- |
| `1. group policy.png`    | ⚙️ Group Policy configuration within the domain    |
| `2. password policy.png` | 🔐 Configured password and account policy settings |

---

## ✅ Validation

The configuration was validated by reviewing the applicable Group Policy settings and confirming that the documented password policy values were configured in the domain environment.

The policy configuration provides a baseline for consistent account security and can also be referenced during future authentication or account-related troubleshooting scenarios.

---

## 💡 Key Takeaway

Group Policy provides centralized control over Windows and security configuration in an Active Directory environment.

This baseline demonstrates practical experience with:

* ⚙️ Group Policy administration
* 🔐 Password policy configuration
* 🛡️ Centralized security settings
* 🔍 Policy validation
* 📝 Technical documentation

The policy settings established here can be referenced when investigating authentication and account-related issues in later scenarios.
