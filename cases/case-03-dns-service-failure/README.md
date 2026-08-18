# 🌐 Case 03 — DNS Service Failure

## 📌 Scenario

NorthBridge reported a DNS resolution problem affecting `MGT-PC01`.

The workstation could communicate with the domain controller, but DNS queries for `northbridge.local` were timing out.

The issue was investigated to determine whether the problem was related to the client, network connectivity, or the DNS server.

---

## 🎫 Incident Details

| Item              | Details                |
| ----------------- | ---------------------- |
| Ticket            | `NB-INC-003`           |
| Client            | `MGT-PC01`             |
| Domain Controller | `SRV-DC01`             |
| Domain            | `northbridge.local`    |
| DNS Server        | `SRV-DC01`             |
| DNS Server IP     | `192.168.29.10`        |
| Issue             | DNS Resolution Failure |
| Status            | pending               |

---

## 👥 Participants

| Participant                                                 | Role             | Repository                                                                           |
| ----------------------------------------------------------- | ---------------- | ------------------------------------------------------------------------------------ |
| [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk) | 📝 Documentation | [Hari's Repository](https://github.com/harikrishnan-rk/Northbridge-Active-Directory) |
| [Mr. Manu P Nair](https://github.com/manunair16)            | 🧑‍💻 Helpdesk   | [Manu's Repository](https://github.com/manunair16/northbridge-active-directory)      |
| [Mr. Varun M Nair](https://github.com/varunmnair95)         | 🛠️ IT Support   | [Varun's Repository](https://github.com/varunmnair95/northbridge-active-directory)   |

---

## 🧑‍💻 My Role — Helpdesk

My responsibility was to perform the initial client-side investigation, reproduce the reported DNS problem, perform basic connectivity checks, collect evidence, and escalate the issue for server-side investigation.

---

## 🔎 Initial Investigation

### 1. Confirmed client configuration

The workstation was confirmed as `MGT-PC01`.

The configured DNS server was:

```text
192.168.29.10
```

📸 Evidence: [client-details](https://github.com/manunair16/northbridge-active-directory/blob/main/cases/case-03-dns-service-failure/evidence/01-client-details.png)

### 2. Tested DNS resolution

DNS resolution for `northbridge.local` was tested.

The request timed out.

A direct DNS lookup against `192.168.29.10` also timed out.

📸 Evidence: [domain-unreachable](https://github.com/manunair16/northbridge-active-directory/blob/main/cases/case-03-dns-service-failure/evidence/02-domain-unreachable.png)

### 3. Checked server connectivity

Connectivity to the DNS server was tested using:

```cmd
ping 192.168.29.10
ping SRV-DC01
```

Both tests were successful.

This showed that the server was reachable even though DNS queries were failing.

📸 Evidence: [server-connectivity](https://github.com/manunair16/northbridge-active-directory/blob/main/cases/case-03-dns-service-failure/evidence/03-ping-reachable.png)

---

## 🧠 Helpdesk Finding

The client was configured to use the expected DNS server and basic connectivity to `SRV-DC01` was available.

However, DNS queries were not receiving a response.

The incident was therefore escalated for server-side investigation.

---

## 🔗 Investigation & Resolution

The server-side investigation and remediation were performed by:

🛠️ **[Varun — IT Support](https://github.com/varunmnair95/northbridge-active-directory/tree/main/cases/case-03-dns-service-failure)**

The DNS Server service on `SRV-DC01` was found to be stopped and was subsequently restored.

---

## ✅ Validation

After the server-side resolution, DNS queries were tested again from `MGT-PC01`.

The lookup successfully returned the DNS server address.

📸 Evidence: [dns-resolution-restored](https://github.com/manunair16/northbridge-active-directory/blob/main/cases/case-03-dns-service-failure/evidence/04-domain-reachable.png)

This confirmed that DNS resolution had been restored.

---

## 💡 Lessons Learned

* 🔎 Check client configuration before making changes.
* 🌐 Test DNS separately from basic network connectivity.
* 📡 Successful ping does not prove that DNS is functioning.
* 📤 A good Helpdesk escalation should provide evidence and useful findings.
* ✅ Always validate the original reported problem after remediation.

---

## 🤝 Collaboration

This case was completed collaboratively by:

* [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk)
* [Mr. Manu P Nair](https://github.com/manunair16)
* [Mr. Varun M Nair](https://github.com/varunmnair95)

The client-side investigation and evidence are maintained in this repository.

The server-side investigation and resolution are documented in [Varun's repository](https://github.com/varunmnair95/northbridge-active-directory/tree/main/cases/case-03-dns-service-failure).

Each participant maintained their own implementation and evidence in an independent NorthBridge Active Directory lab.
