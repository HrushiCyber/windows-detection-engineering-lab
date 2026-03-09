# Detection: SAM Database Dump

ATT&CK Technique: T1003.002
Tactic: Credential Access

## Adversary Behavior

Attackers may extract password hashes from the **Security Account Manager (SAM)** database.

The SAM database stores local account credentials and is located at:

```
C:\Windows\System32\config\SAM
```

Attackers often combine SAM dumping with SYSTEM hive extraction.

## Telemetry Signals

Relevant endpoint telemetry:

• File access to SAM database
• Access to SYSTEM registry hive
• Suspicious execution of credential dumping tools

## Detection Logic

Alert when:

• Non-system process accesses SAM database
• Tools like `reg.exe` or `esentutl.exe` access sensitive registry files

## Investigation Steps

1 Identify the process accessing SAM
2 Review command line arguments
3 Determine if activity is authorized administrative activity

## False Positives

System backups or forensic tools accessing registry files.
