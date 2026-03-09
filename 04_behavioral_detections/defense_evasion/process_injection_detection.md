# Detection: Process Injection

ATT&CK Technique: T1055

Attackers inject malicious code into legitimate processes.

---

## Detection Signals

• CreateRemoteThread
• WriteProcessMemory
• Suspicious memory allocation

---

## Investigation

Identify source process and injected target process.


====================================================================================
# Detection: Process Injection

MITRE ATT&CK Technique: T1055
Tactic: Defense Evasion

---

# Overview

Process injection allows attackers to execute malicious code within the memory space of legitimate processes.

This technique helps attackers evade detection and hide malicious activity.

---

# Adversary Tradecraft

Common process injection methods include:

• DLL injection
• reflective DLL injection
• process hollowing
• thread injection

Attackers frequently inject payloads into trusted processes such as:

```
explorer.exe
svchost.exe
lsass.exe
```

---

# Real World Attack Scenario

```
initial malware execution
        ↓
payload injected into explorer.exe
        ↓
malware hides within legitimate process
        ↓
command and control communication
```

---

# Endpoint Telemetry

EDR telemetry may capture:

• memory allocation events
• remote thread creation
• suspicious process memory writes

Common API calls involved in process injection:

```
OpenProcess
WriteProcessMemory
CreateRemoteThread
```

---

# Detection Logic

Alert when:

• one process writes memory into another process
• remote threads are created in critical system processes
• unsigned processes inject code into trusted applications

---

# Investigation Workflow

1 Identify source process performing injection
2 Identify target process receiving injected code
3 Analyze injected memory region
4 Determine whether activity matches legitimate application behavior
