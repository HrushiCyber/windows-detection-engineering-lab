# Detection: WMIC Remote Execution

ATT&CK Technique: T1047
Tactic: Execution

## Adversary Behavior

Attackers use Windows Management Instrumentation (WMI) for remote command execution.

## Detection Signals

• WMIC commands executed with remote targets
• Suspicious process chains

## Investigation

Identify remote system and executed command.
