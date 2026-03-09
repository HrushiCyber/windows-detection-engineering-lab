# Detection: Suspicious MSHTA Execution

ATT&CK Technique: T1218.005
Tactic: Execution

## Adversary Behavior

Attackers abuse `mshta.exe` to execute malicious scripts.

MSHTA allows execution of HTML applications and scripts.

## Detection Logic

Alert when:

• `mshta.exe` executes scripts from remote URLs
• Parent process is suspicious (Office, browser)

## Investigation

Review command line parameters and script content.
