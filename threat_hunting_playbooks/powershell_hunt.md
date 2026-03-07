# Threat Hunting Playbook: PowerShell Abuse

PowerShell is frequently used by attackers.

---

## Suspicious Indicators

Encoded commands
Download cradles
AMSI bypass attempts

---

## Example Query Logic

Search for:

```
powershell.exe -EncodedCommand
```

---

## Investigation

Review command line arguments and parent processes.
