# Detection: Command and Control Beaconing

ATT&CK Technique: T1071

Malware frequently communicates with command-and-control servers using periodic connections.

---

## Detection Signals

Regular outbound connections at fixed intervals.

---

## Investigation

Analyze destination IP reputation and network patterns.

============================================================================================================
# Detection: Command and Control Beaconing

MITRE ATT&CK Technique: T1071
Tactic: Command and Control

---

# Overview

Many malware families communicate with command-and-control servers using periodic network connections known as **beaconing**.

---

# Adversary Tradecraft

Beaconing malware typically connects to remote servers at regular intervals.

Example pattern:

```
every 60 seconds → HTTP request
```

This communication allows attackers to issue commands to compromised systems.

---

# Endpoint Telemetry

Relevant telemetry includes:

• network connection logs
• DNS queries
• process responsible for network traffic

---

# Detection Logic

Alert when:

• network connections occur at consistent intervals
• processes repeatedly contact the same external IP
• unusual processes generate outbound connections

