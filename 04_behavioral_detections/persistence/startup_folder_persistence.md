# Detection: Startup Folder Persistence

MITRE ATT&CK Technique: T1547.001
Tactic: Persistence

---

# Overview

The Windows Startup folder allows applications to execute automatically when a user logs in.

Attackers frequently place malicious executables or scripts inside this directory.

---

# Adversary Tradecraft

Common startup folder locations:

```
C:\Users\<user>\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup
C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup
```

Malware placed in these directories executes automatically during user logon.

---

# Endpoint Telemetry

EDR platforms monitor:

• file creation events
• process responsible for file creation
• execution of files located in startup directories

---

# Detection Logic

Alert when:

• executable files are written to Startup directories
• suspicious processes create startup folder files

---

# Investigation Workflow

1 Identify file written to startup folder
2 Determine parent process responsible
3 Verify digital signature of executable
4 Analyze file for malicious behavior
