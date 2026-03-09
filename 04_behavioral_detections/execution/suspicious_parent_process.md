# Detection: Suspicious Parent Process Chain

MITRE ATT&CK Technique: T1059
Tactic: Execution

---

# Overview

Process relationships reveal valuable behavioral indicators.

Certain parent-child process combinations are rarely seen during legitimate activity.

---

# Adversary Tradecraft

Attackers often abuse scripting engines and system utilities.

Example suspicious chains:

```
winword.exe → powershell.exe
chrome.exe → cmd.exe
explorer.exe → mshta.exe
```

---

# Detection Logic

Alert when unusual process lineage occurs between:

• user applications
• command shells
• scripting engines

---

# Investigation Workflow

1 Identify parent process
2 Review command line arguments
3 Investigate associated files or scripts
