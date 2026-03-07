# Threat Hunting Playbook: Credential Dumping

Credential dumping is a common attacker technique.

---

## Objective

Detect suspicious access to the LSASS process.

---

## Telemetry Sources

Sysmon Event ID 10
EDR process access telemetry

---

## Hunt Hypothesis

Processes requesting memory access to LSASS are suspicious.

---

## Investigation Steps

1. Identify source process
2. Check command line
3. Verify digital signature
4. Analyze parent process
