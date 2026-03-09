# Detection: Cached Credential Extraction

ATT&CK Technique: T1003.004
Tactic: Credential Access

## Adversary Behavior

Windows stores cached domain credentials to allow offline authentication.

Attackers extract cached credentials from registry keys such as:

```
HKLM\Security\Cache
```

## Telemetry Signals

• Registry access to cached credential keys
• Privileged processes accessing registry hives

## Detection Logic

Alert when unauthorized processes attempt to access cached credential registry locations.

## Investigation

Determine if the process accessing cached credentials is legitimate or malicious.
