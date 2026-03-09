# Detection: AMSI Bypass

MITRE ATT&CK Technique: T1562
Tactic: Defense Evasion

---

# Overview

AMSI (Antimalware Scan Interface) allows security software to inspect scripts before execution.

Attackers bypass AMSI to run malicious PowerShell payloads undetected.

---

# Adversary Tradecraft

Common AMSI bypass techniques:

• patching AMSI memory
• disabling AMSI scanning functions
• obfuscating PowerShell scripts

---

# Endpoint Telemetry

Relevant signals include:

• suspicious PowerShell script execution
• memory modification of AMSI functions

---

# Detection Logic

Alert when PowerShell processes attempt to disable AMSI scanning.
