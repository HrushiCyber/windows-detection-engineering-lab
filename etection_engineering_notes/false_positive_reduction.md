# False Positive Reduction

False positives reduce SOC efficiency.

Detection engineers must implement tuning strategies.

## Common Sources of False Positives

Security software
Administrative scripts
Backup agents

---

## Strategies

### Parent Process Analysis

Example:

```
winword.exe → powershell.exe
```

Often suspicious.

---

### Code Signature Verification

Check if executable is signed by trusted vendors.

---

### Command Line Analysis

Example suspicious patterns:

```
powershell.exe -EncodedCommand
```
