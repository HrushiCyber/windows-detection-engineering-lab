# Detection: Cached Domain Credentials Extraction

MITRE ATT&CK Technique: T1003.004
Tactic: Credential Access

---

# Overview

Windows systems cache domain credentials locally to allow users to authenticate when a domain controller is unavailable. These cached credentials are stored in the Windows registry and can be extracted by attackers to obtain password hashes.

Attackers often target cached credentials after gaining administrative privileges on a workstation.

---

# Adversary Tradecraft

Cached credentials are stored in the following registry location:

```
HKLM\Security\Cache
```

Attackers extract these values using tools such as:

• Mimikatz
• secretsdump.py (Impacket)
• Windows Registry utilities

The extracted hashes can be used for:

• offline password cracking
• pass-the-hash attacks
• lateral movement

---

# Real World Attack Scenario

A common attack chain may look like:

```
initial compromise
      ↓
privilege escalation
      ↓
cached credential extraction
      ↓
credential reuse across domain systems
```

---

# Endpoint Telemetry

Relevant EDR telemetry includes:

• registry hive access
• privileged registry queries
• suspicious processes accessing security registry keys

Monitoring access to the following registry path is important:

```
HKLM\Security\Cache
```

---

# Detection Logic

Detection should trigger when:

• non-system processes access cached credential registry keys
• administrative tools access security hives unexpectedly
• suspicious parent-child process chains interact with registry security hives

---

# Investigation Workflow

1 Identify the process accessing cached credential keys
2 Review command line parameters
3 Determine whether activity originated from legitimate administration
4 Investigate host for additional credential dumping activity

---

# Potential False Positives

Some legitimate forensic tools may access cached credential registry locations.

Analysts should verify:

• binary reputation
• digital signatures
• administrative context
