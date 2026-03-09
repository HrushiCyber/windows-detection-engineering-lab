# Detection: Office Application Spawning Shell

ATT&CK Technique: T1204
Tactic: Execution

## Adversary Behavior

Malicious Office documents may spawn command shells.

Example chain:

```
winword.exe → powershell.exe
```

## Detection Logic

Alert when Office applications spawn:

• cmd.exe
• powershell.exe
• wscript.exe
