# Detection: LSASS Memory Access

ATT&CK Technique: T1003.001
Tactic: Credential Access

---

## Adversary Behavior

Attackers read LSASS memory to extract credentials.

---

## Telemetry Signals

EDR platforms detect handle access to the LSASS process.

Example pattern:

```
Process → lsass.exe
AccessMask → PROCESS_VM_READ
```

---

## Detection Logic

Trigger alerts when:

• Non-system processes access LSASS memory
• Unsigned processes access LSASS
• Suspicious parent processes interact with LSASS

---

## Investigation

1 Identify the source process
2 Verify binary signature
3 Check command line arguments
4 Investigate host activity

---

## Potential False Positives

Security software or EDR agents accessing LSASS.
