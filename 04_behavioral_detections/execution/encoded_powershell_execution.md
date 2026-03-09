# Detection: Encoded PowerShell Execution

ATT&CK Technique: T1059.001
Tactic: Execution

---

## Adversary Behavior

Attackers encode PowerShell commands to hide malicious activity.

Example command:

```
powershell.exe -EncodedCommand
```

---

## Detection Logic

Alert when PowerShell is executed with encoded commands.

---

## Investigation

Decode the Base64 payload and analyze the script.
