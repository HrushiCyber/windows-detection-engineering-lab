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
