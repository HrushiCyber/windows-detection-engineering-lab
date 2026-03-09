# Detection: PsExec Lateral Movement

ATT&CK Technique: T1021.002

PsExec allows remote command execution.

---

## Detection Signals

Look for service name:

```
PSEXESVC
```

---

## Investigation

Identify source host and authentication method used.

==========================================================================================
# Detection: PsExec Lateral Movement

MITRE ATT&CK Technique: T1021.002
Tactic: Lateral Movement

---

# Overview

PsExec is a legitimate administrative tool used to execute commands on remote systems.

Attackers frequently abuse PsExec for lateral movement across networks.

---

# Adversary Tradecraft

PsExec copies a service binary to the target system and executes it remotely.

Example command:

```
psexec \\target-host cmd.exe
```

The tool creates a service named:

```
PSEXESVC
```

---

# Endpoint Telemetry

Relevant signals include:

• service creation events
• SMB network connections
• remote command execution

---

# Detection Logic

Alert when:

• service named `PSEXESVC` is created
• remote service creation occurs between workstations
• unusual authentication events accompany service creation

---

# Investigation Workflow

1 Identify source host initiating PsExec
2 Review user account used for authentication
3 Verify command executed on target system
