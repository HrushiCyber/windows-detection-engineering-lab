# Detection: Suspicious Rundll32 Execution

MITRE ATT&CK Technique: T1218.011
Tactic: Execution

---

# Overview

`rundll32.exe` is a Windows utility used to execute functions exported from DLL files.

Attackers frequently abuse rundll32 to execute malicious code.

---

# Adversary Tradecraft

Example malicious command:

```
rundll32.exe malicious.dll,EntryPoint
```

Attackers may execute DLLs from:

• temporary directories
• user download folders
• network shares

---

# Endpoint Telemetry

Key telemetry signals include:

• rundll32 command line parameters
• DLL file path
• parent process relationship

Example suspicious chain:

```
powershell.exe → rundll32.exe
```

---

# Detection Logic

Alert when:

• rundll32 executes DLLs from suspicious directories
• command line contains abnormal parameters
• parent process is unexpected
