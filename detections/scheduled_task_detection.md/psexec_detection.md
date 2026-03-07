# PsExec Lateral Movement Detection

ATT&CK Technique: T1021.002

---

## Tradecraft

PsExec enables remote command execution via SMB.

---

## Telemetry

Service creation events
SMB network activity

---

## Detection

Look for service name:

```
PSEXESVC
```
