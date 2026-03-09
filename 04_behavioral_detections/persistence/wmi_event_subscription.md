# Detection: WMI Event Subscription Persistence

MITRE ATT&CK Technique: T1546.003
Tactic: Persistence

---

# Overview

Windows Management Instrumentation (WMI) event subscriptions can execute scripts automatically when specific system events occur.

Attackers use this mechanism to maintain stealthy persistence.

---

# Adversary Tradecraft

Attackers create three components:

• WMI Event Filter
• WMI Consumer
• Binding between filter and consumer

These components trigger malicious scripts during specific events.

---

# Endpoint Telemetry

Relevant telemetry includes:

• WMI subscription creation events
• PowerShell or script execution triggered by WMI

---

# Detection Logic

Alert when:

• new WMI event subscriptions are created
• WMI consumers execute suspicious commands
