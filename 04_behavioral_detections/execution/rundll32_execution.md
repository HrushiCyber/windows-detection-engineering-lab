# Detection: Suspicious Rundll32 Execution

ATT&CK Technique: T1218.011
Tactic: Execution

## Adversary Behavior

Attackers abuse `rundll32.exe` to execute malicious DLLs.

## Detection Signals

• Rundll32 loading DLLs from temporary directories
• Suspicious command line parameters

## Investigation

Verify DLL path and process parent chain.
