# Detection: Scheduled Task Persistence

ATT&CK Technique: T1053.005

Attackers create scheduled tasks to maintain persistence.

---

## Detection Signals

Monitor scheduled task creation events.

Windows Event ID:

```
4698
```

---

## Investigation

Review task command and associated binary.


==================================================================================================
# Detection: Scheduled Task Persistence

MITRE ATT&CK Technique: T1053.005
Tactic: Persistence

---

# Overview

Windows scheduled tasks allow programs to execute automatically at specific times or events.

Attackers often create malicious scheduled tasks to maintain persistence on compromised systems.

---

# Adversary Tradecraft

Example attacker command:

```
schtasks /create /sc minute /mo 5 /tn updater /tr C:\malware.exe
```

This task executes malware every 5 minutes.

Scheduled tasks can also trigger:

• at system startup
• during user logon
• at specific time intervals

---

# Real World Attack Scenario

```
initial compromise
       ↓
payload execution
       ↓
scheduled task creation
       ↓
persistent malware execution
```

---

# Endpoint Telemetry

Relevant telemetry sources:

• Windows Security Event Logs
• Task Scheduler logs
• process creation events

Key event ID:

```
4698
```

This event indicates a scheduled task was created.

---

# Detection Logic

Alert when:

• new scheduled tasks are created by suspicious processes
• scheduled task commands reference executables in temporary directories
• scheduled tasks execute scripts or PowerShell commands

---

# Investigation Workflow

1 Identify the user who created the scheduled task
2 Review the command executed by the task
3 Verify file referenced in the task configuration
4 Investigate host for additional persistence mechanisms
