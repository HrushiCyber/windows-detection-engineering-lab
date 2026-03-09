# Persistence Tradecraft

Persistence techniques allow attackers to maintain access to compromised systems.

---

# Common Persistence Techniques

### Scheduled Tasks

Attackers create scheduled tasks to execute malicious payloads periodically.

---

### Registry Run Keys

Attackers add entries to registry run keys to execute malware at system startup.

Example locations:

```
HKCU\Software\Microsoft\Windows\CurrentVersion\Run
```

---

### Startup Folder

Executables placed in the Windows startup folder execute when the user logs in.

---

### WMI Event Subscriptions

WMI event subscriptions can trigger malicious code when specific system events occur.
