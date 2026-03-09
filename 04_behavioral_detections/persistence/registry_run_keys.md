# Detection: Registry Run Key Persistence

ATT&CK Technique: T1547.001
Tactic: Persistence

## Behavior

Attackers modify Run keys to execute malware during login.

Registry locations include:

```
HKCU\Software\Microsoft\Windows\CurrentVersion\Run
```

## Detection Logic

Alert when executables are added to Run keys.
