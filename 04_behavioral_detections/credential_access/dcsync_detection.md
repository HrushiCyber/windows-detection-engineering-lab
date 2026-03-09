# Detection: DCSync Attack

ATT&CK Technique: T1003.006
Tactic: Credential Access

## Adversary Behavior

The DCSync technique abuses directory replication to retrieve password hashes.

Attackers impersonate domain controllers and request password data from Active Directory.

## Telemetry Signals

• Directory replication requests
• Unusual replication operations from non-domain controllers

## Detection Logic

Alert when directory replication occurs from unexpected hosts.

## Investigation

Verify if the system performing replication is an authorized domain controller.
