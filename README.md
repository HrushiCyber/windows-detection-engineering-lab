# Windows Detection Engineering Lab

This repository documents practical **endpoint detection engineering techniques** used in modern Security Operations Centers (SOC).

The goal is to map **attacker tradecraft → endpoint telemetry → detection logic**.

---

## Focus Areas

• Windows endpoint telemetry
• Behavioral detections
• Threat hunting playbooks
• Detection engineering methodology
• SIEM query examples

---

## Telemetry Sources

The detections in this repository rely on common endpoint telemetry:

* Windows Security Event Logs
* Sysmon
* EDR process telemetry
* Network telemetry

---

## SIEM Query Examples

Queries are provided for:

* Microsoft Sentinel (KQL)
* Splunk (SPL)
* Elastic Security (EQL)

---

## Detection Coverage

Credential Access
Execution
Persistence
Lateral Movement

---

## Repository Structure

```
detections/                    Detection writeups
queries/                       SIEM queries
telemetry_maps/                Endpoint telemetry reference
threat_hunting_playbooks/      Threat hunting guides
detection_engineering_notes/   Detection methodology
```

---

## Purpose

This repository demonstrates practical skills in:

* Detection engineering
* Endpoint telemetry analysis
* Threat hunting
* SOC investigation workflows

---

## Disclaimer

All techniques described in this repository are for **defensive security research and detection development only**.
