# Detection: Service Permission Abuse

MITRE ATT&CK Technique: T1574
Tactic: Privilege Escalation

---

# Overview

Windows services may have weak permissions allowing attackers to modify service binaries.

This allows attackers to replace legitimate executables with malicious payloads.

---

# Adversary Tradecraft

Attackers identify vulnerable services using tools such as:

```
accesschk
PowerUp
Seatbelt
```

They then replace the service executable with a malicious payload.

---

# Detection Logic

Alert when:

• service executable paths are modified
• service configuration changes occur unexpectedly
