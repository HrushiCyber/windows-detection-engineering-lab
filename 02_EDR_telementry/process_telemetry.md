# Process Telemetry

Process creation telemetry is one of the most important signals for detection engineering.

---

# Process Creation Events

Typical attributes collected by EDR platforms include:

• process name
• command line arguments
• parent process
• process ID
• user context

---

# Detection Opportunities

Detection engineers analyze process telemetry to identify:

• suspicious parent-child relationships
• unusual command line parameters
• execution of known attacker tools

---

# Examples

Suspicious process chains:

```
winword.exe → powershell.exe
```

```
chrome.exe → cmd.exe
```

These patterns often indicate malicious activity.
