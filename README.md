# Windows Detection Engineering Lab

This repository is a **technical knowledge base for Windows Endpoint Detection and Response (EDR) detection engineering**.

The objective of this project is to demonstrate how detection engineers design **behavior-based detections** by combining:

• Windows internals knowledge
• Endpoint telemetry analysis
• Adversary tradecraft understanding
• Detection engineering methodology

Instead of relying on static indicators, this repository focuses on **behavioral detection logic derived from attacker techniques**.

---

# Why This Repository Exists

Most public security repositories focus on:

• IOC collections
• Sigma rules
• simple SIEM queries

However, effective endpoint detection requires deeper understanding of:

• Windows architecture
• process and memory operations
• attacker tradecraft
• endpoint telemetry sources

This repository aims to bridge that gap.

---

# Repository Structure

## 01 Windows Internals

Understanding Windows architecture is essential for designing reliable detections.

Topics include:

• Windows process architecture
• Windows memory model
• authentication architecture
• Windows security subsystem
• process injection techniques

---

## 02 EDR Telemetry

Endpoint detection platforms rely on telemetry from operating system events.

This section explains how telemetry is generated and how it can be used for detection.

Examples include:

• process creation telemetry
• file system activity
• registry modification events
• network connection telemetry
• handle access monitoring

---

## 03 Adversary Tradecraft

Detection engineers must understand attacker techniques.

This section documents common attacker behaviors mapped to MITRE ATT&CK.

Examples include:

• credential dumping
• lateral movement techniques
• persistence mechanisms
• defense evasion strategies
• command and control activity

---

## 04 Behavioral Detections

This section contains behavior-based detections designed using:

• Windows telemetry
• adversary techniques
• endpoint signals

---

## 05 Detection Engineering

Detection engineering is an iterative process.

This section documents the frameworks used to build high-fidelity detections.

Topics include:

• detection design methodology
• detection lifecycle
• false positive reduction
• detection validation

---

## 06 SOC Investigation Playbooks

Detection alone is not sufficient.

SOC analysts must investigate alerts effectively.

This section documents investigation workflows for common alerts.

---

## 07 Detection Research

Advanced research topics for detection engineering.

Examples:

• process injection detection
• PowerShell tradecraft
• living-off-the-land binaries
• command and control beaconing

---

## 08 Detection Coverage

Mapping behavioral detections to the MITRE ATT&CK framework.

---

# Intended Audience

This repository is intended for:

• SOC analysts
• detection engineers
• threat hunters
• security engineers
• blue team practitioners

---

# Disclaimer

This repository is intended for **defensive security research and detection engineering education only**.
