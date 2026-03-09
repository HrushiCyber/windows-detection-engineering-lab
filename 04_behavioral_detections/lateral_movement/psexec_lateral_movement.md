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
