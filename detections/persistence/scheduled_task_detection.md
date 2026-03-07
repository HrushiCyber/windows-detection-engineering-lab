# Scheduled Task Persistence

ATT&CK Technique: T1053.005

---

## Tradecraft

Attackers create scheduled tasks for persistence.

Example command:

```
schtasks /create
```

---

## Telemetry

Windows Event ID:

```
4698
```

---

## Detection

Monitor creation of new scheduled tasks by unusual users.
