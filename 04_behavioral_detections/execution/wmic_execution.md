# Detection: WMIC Execution

MITRE ATT&CK Technique: T1047
Tactic: Execution

---

# Overview

Windows Management Instrumentation Command-line (WMIC) enables administrative management of systems.

Attackers abuse WMIC to execute commands locally or remotely.

---

# Adversary Tradecraft

Example malicious command:

```
wmic process call create "cmd.exe /c payload"
```

Attackers frequently use WMIC for lateral movement or remote command execution.

---

# Endpoint Telemetry

Relevant telemetry signals:

• process creation events
• command line arguments
• network connections associated with remote WMI calls

---

# Detection Logic

Alert when:

• WMIC executes suspicious commands
• WMIC spawns command shells
• WMIC execution originates from user applications
