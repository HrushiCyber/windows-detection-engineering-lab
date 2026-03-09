# Detection: DLL Search Order Hijacking

MITRE ATT&CK Technique: T1574.001
Tactic: Defense Evasion

---

# Overview

Windows loads DLL files using a defined search order.

Attackers place malicious DLLs in directories where applications will load them first.

---

# Detection Logic

Alert when DLLs are loaded from:

• temporary directories
• user profile folders
• network shares
