# Detection Engineering Methodology

Detection engineering translates attacker behavior into detection logic.

---

## Detection Design Workflow

Attacker Technique
↓
Telemetry Source
↓
Detection Hypothesis
↓
Detection Query
↓
Validation
↓
False Positive Tuning

---

## Example

Technique: LSASS Credential Dumping

Telemetry:

Sysmon Event ID 10
EDR Handle Access Telemetry

Detection Hypothesis:

Processes requesting memory access to `lsass.exe` are suspicious.
