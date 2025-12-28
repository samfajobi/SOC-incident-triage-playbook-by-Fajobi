
When we **map an attack to MITRE ATT&CK**, we are mapping **what the attacker did** (their **actions and behaviors**) to **standardized techniques and tactics** in the ATT&CK framework.

We are **NOT** mapping:

* Tools
* Malware names
* CVE numbers
* IP addresses

We are mapping **attacker behavior**.

---

## What exactly are we mapping?

We map **observed attack activities** to:

### 1️⃣ **Tactics** (the *WHY*)

The attacker’s **goal at that stage** of the attack.

Examples:

* Initial Access
* Execution
* Persistence
* Privilege Escalation
* Defense Evasion
* Credential Access
* Command and Control

---

### 2️⃣ **Techniques** (the *HOW*)

The **method** used to achieve that goal.

Examples:

* `T1059` – Command and Scripting Interpreter
* `T1071.004` – DNS for C2
* `T1003` – Credential Dumping
* `T1055` – Process Injection

---

### 3️⃣ **Sub-techniques** (the *exact method*)

More specific behavior.

Example:

* `T1059.001` – PowerShell
* `T1071.004` – DNS C2

---

## Real-world example (SOC-style)

### Alert observed:

* Suspicious PowerShell execution
* Encoded command
* Outbound DNS requests to random-looking domains

### Mapping:

| Observation          | MITRE Mapping                                                 |
| -------------------- | ------------------------------------------------------------- |
| PowerShell execution | **Execution – T1059.001 (PowerShell)**                        |
| Encoded command      | **Defense Evasion – T1027 (Obfuscated Files or Information)** |
| DNS beaconing        | **Command and Control – T1071.004 (DNS)**                     |

👉 You are mapping **each malicious action** to a MITRE technique.

---



