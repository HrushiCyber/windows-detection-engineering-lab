# Encoded PowerShell Detection

ATT&CK Technique: T1059.001

---

## Adversary Tradecraft

Attackers encode PowerShell commands to evade detection.

Example:

```
powershell.exe -EncodedCommand <base64>
```

---

## Telemetry

Process creation logs.

---

## Detection Logic

Look for PowerShell executions containing the parameter:

```
-EncodedCommand
```

---

## False Positives

Rare but may occur during automation scripts.
