# Detection: Registry Run Key Persistence

MITRE ATT&CK Technique: T1547.001
Tactic: Persistence

---

# Overview

Windows registry Run keys allow applications to automatically execute when a user logs in.

Attackers frequently abuse these registry keys to maintain persistence on compromised systems.

---

# Adversary Tradecraft

Common registry locations abused for persistence:

```
HKCU\Software\Microsoft\Windows\CurrentVersion\Run
HKLM\Software\Microsoft\Windows\CurrentVersion\Run
```

Attackers add malicious executables or scripts that execute automatically during system startup.

Example command:

```
reg add HKCU\Software\Microsoft\Windows\CurrentVersion\Run /v updater /t REG_SZ /d C:\malware.exe
```

---

# Real World Attack Scenario

```
initial compromise
      ↓
payload execution
      ↓
registry run key creation
      ↓
malware persistence after reboot
```

---

# Endpoint Telemetry

EDR telemetry signals include:

• registry modification events
• process responsible for registry changes
• command line parameters used to modify registry keys

---

# Detection Logic

Alert when:

• new values are added to Run keys
• unsigned executables are referenced in Run entries
• unusual processes modify persistence registry locations

---

# Investigation Workflow

1 Identify process modifying registry key
2 Verify executable referenced in Run entry
3 Check binary reputation and signature
4 Investigate host for additional persistence mechanisms
