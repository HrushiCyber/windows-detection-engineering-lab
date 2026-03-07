# Windows EDR Telemetry Reference

Modern EDR platforms collect extensive telemetry from endpoints.

---

## Process Creation

Fields collected:

• Process name
• Command line
• Parent process
• Integrity level
• File path

Detection uses:

Parent-child relationships
Suspicious command lines

---

## Handle Access

Critical for detecting:

Credential dumping
Process injection

Example:

```
Process → lsass.exe
AccessMask → PROCESS_VM_READ
```

---

## Network Connections

Used to detect:

Command and control traffic
Beaconing activity

---

## File Creation

Tracks malware staging.

Example detection:

Executable dropped in temporary directory.

---

## Registry Changes

Used to detect persistence techniques such as Run keys.
    