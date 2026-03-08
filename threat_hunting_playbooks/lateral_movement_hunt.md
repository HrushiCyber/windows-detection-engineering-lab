# Threat Hunting Playbook: Lateral Movement

Lateral movement allows attackers to expand access across the network.

---

## Common Tools

PsExec
WMI
Remote Service Creation

---

## Telemetry Sources

Windows Event Logs
Network logs
Process creation events

---

## Hunt Hypothesis

Remote execution from non-administrative workstations is suspicious.

---

## Investigation Steps

1 Identify source host
2 Check authentication logs
3 Investigate executed commands
