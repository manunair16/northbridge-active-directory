# 🔐 Case 02 — Account Lockout

## 📌 Scenario

Kevin Thomas, an Operations Executive, reported that he could not sign in to `OPS-PC01` because his NorthBridge domain account was locked.

The issue was intentionally simulated in the isolated NorthBridge Active Directory lab.

---

## 🎫 Incident Details

| Item              | Details             |
| ----------------- | ------------------- |
| Ticket            | `NB-INC-002`        |
| User              | Kevin Thomas        |
| Department        | Operations          |
| Client            | `OPS-PC01`          |
| Domain Controller | `SRV-DC01`          |
| Domain            | `northbridge.local` |
| Issue             | Account Lockout     |
| Status            | Resolved            |

---

## 👥 Participants

| Participant                                                 | Role             | Repository                                                                           |
| ----------------------------------------------------------- | ---------------- | ------------------------------------------------------------------------------------ |
| [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk) | 🛠️ IT Support   | [Hari's Repository](https://github.com/harikrishnan-rk/Northbridge-Active-Directory) |
| [Mr. Manu P Nair](https://github.com/manunair16)            | 📝 Documentation | [Manu's Repository](https://github.com/manunair16/northbridge-active-directory)      |
| [Mr. Varun M Nair](https://github.com/varunmnair95)         | 🧑‍💻 Helpdesk   | [Varun's Repository](https://github.com/varunmnair95/northbridge-active-directory)   |

---

## 📝 My Role — Documentation

My responsibility was to document the incident, consolidate the findings from the Helpdesk and IT Support roles, record the resolution, and confirm the final validation.

---

## 🕒 Incident Flow

```text
🚨 User Report
      ↓
🧑‍💻 Helpdesk Triage
      ↓
🔎 Active Directory Investigation
      ↓
🎯 Root Cause
      ↓
🛠️ Remediation
      ↓
🔓 Account Restored
      ↓
✅ Validation
      ↓
📝 Case Closure
```

---

## 🔎 Investigation Summary

### Helpdesk

Initial troubleshooting was performed by:

🧑‍💻 **[Varun — Helpdesk](https://github.com/varunmnair95/northbridge-active-directory)**

The login failure was reproduced and basic client-to-domain-controller connectivity was checked.

### IT Support

Active Directory investigation was performed by:

🛠️ **[Hari — IT Support](https://github.com/harikrishnan-rk/Northbridge-Active-Directory)**

The account lockout and relevant Security event evidence were investigated.

---

## 🎯 Root Cause

**The user exceeded the maximum allowed number of failed login attempts.**

---

## 🛠️ Resolution

The identified cause was addressed and Kevin's account was unlocked.

---

## ✅ Validation

Kevin successfully authenticated to `OPS-PC01` after remediation.

The successful validation evidence is maintained in this repository.

📸 Evidence: [user-login-success-validation](validation/1-user-login-success-validation.png)

---

## 💡 Lessons Learned

* 🔐 Account lockouts should be investigated before simply unlocking the account.
* 🔎 Security event evidence helps identify the source of authentication failures.
* 🧠 Troubleshooting should move from symptom to root cause.
* ✅ Successful authentication confirms that the remediation restored access.
* 📝 Clear documentation makes the investigation understandable to another technician.

---

## 🤝 Collaboration

This case was completed collaboratively by:

* [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk)
* [Mr. Manu P Nair](https://github.com/manunair16)
* [Mr. Varun M Nair](https://github.com/varunmnair95)

Each participant maintained their own implementation and evidence in an independent NorthBridge Active Directory lab.

