# Detection: Process Injection

ATT&CK Technique: T1055

Attackers inject malicious code into legitimate processes.

---

## Detection Signals

• CreateRemoteThread
• WriteProcessMemory
• Suspicious memory allocation

---

## Investigation

Identify source process and injected target process.
