# Detection: Windows Service Persistence

MITRE ATT&CK Technique: T1543
Tactic: Persistence

---

# Overview

Windows services allow software to run in the background.

Attackers frequently create malicious services to maintain persistence.

---

# Adversary Tradecraft

Example command used by attackers:

```
sc create backdoor binpath= C:\malware.exe
```

The malicious service will start automatically when the system boots.

---

# Endpoint Telemetry

Relevant telemetry signals:

• service creation events
• service binary path
• service start events

Windows Event ID:

```
7045
```

---

# Detection Logic

Alert when:

• new services are created by suspicious processes
• service binaries reside in user directories

---

# Investigation Workflow

1 Identify service creation event
2 Review binary path associated with service
3 Analyze executable referenced by service
