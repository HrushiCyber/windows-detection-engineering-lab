# LSASS Memory Access Detection

ATT&CK Technique: T1003.001

---

## Adversary Tradecraft

Attackers dump credentials from LSASS memory.

Common tools:

Mimikatz
ProcDump

---

## Telemetry

Sysmon Event ID 10
EDR handle access telemetry

---

## Detection Logic

Processes requesting memory access to `lsass.exe`.

---

## Validation

Example:

```
procdump.exe -ma lsass.exe lsass.dmp
```
