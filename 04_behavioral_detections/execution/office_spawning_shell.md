# Detection: Office Application Spawning Shell

MITRE ATT&CK Technique: T1204
Tactic: Execution

---

# Overview

Office applications should not normally spawn command shells.

Attackers exploit macros or embedded scripts to execute system commands.

---

# Adversary Tradecraft

Example process chain:

```
winword.exe → cmd.exe
winword.exe → powershell.exe
excel.exe → wscript.exe
```

These chains often indicate malicious macro execution.

---

# Endpoint Telemetry

Relevant telemetry includes:

• process creation events
• parent-child process relationships
• command line arguments

---

# Detection Logic

Alert when Office applications spawn:

• PowerShell
• cmd.exe
• wscript.exe
