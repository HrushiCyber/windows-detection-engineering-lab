# Detection: DCSync Attack

MITRE ATT&CK Technique: T1003.006
Tactic: Credential Access

---

# Overview

DCSync is a technique where attackers impersonate a domain controller to request password data from Active Directory using the Directory Replication Service (DRS) protocol.

This technique allows attackers to retrieve password hashes for any domain user.

---

# Adversary Tradecraft

Tools such as **Mimikatz** implement the DCSync technique by issuing replication requests using the following API:

```
DRSUAPI
```

Attackers require the following privileges:

• Replicating Directory Changes
• Replicating Directory Changes All

These privileges are often granted to domain administrators.

---

# Real World Attack Scenario

A typical attack flow:

```
compromise domain admin
      ↓
execute mimikatz DCSync
      ↓
dump domain password hashes
      ↓
full domain compromise
```

---

# Endpoint Telemetry

Relevant telemetry sources include:

• domain controller security logs
• directory replication events
• authentication activity from unusual hosts

Suspicious replication requests originating from non-domain controllers may indicate DCSync activity.

---

# Detection Logic

Detection should trigger when:

• directory replication requests originate from non-domain controller systems
• suspicious processes attempt directory replication operations
• abnormal Active Directory replication activity occurs

---

# Investigation Workflow

1 Identify host performing replication
2 Confirm whether host is a legitimate domain controller
3 Review authentication context
4 Investigate suspicious account privileges

---

# Detection Engineering Notes

Monitoring domain replication behavior is critical for detecting advanced credential theft attacks.

Combining Active Directory logs with endpoint telemetry significantly improves detection reliability.
