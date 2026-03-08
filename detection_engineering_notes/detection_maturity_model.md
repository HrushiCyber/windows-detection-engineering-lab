# Detection Maturity Model

Detection engineering evolves through multiple maturity levels.

## Level 1 – Indicator Based Detection

Relies on static indicators such as:

• File hashes
• IP addresses
• Domains

These detections are easily bypassed when attackers modify infrastructure.

---

## Level 2 – Tool Based Detection

Detects known attacker tools.

Examples:

• mimikatz.exe
• procdump.exe

Limitation: attackers can rename tools.

---

## Level 3 – Behavioral Detection

Focuses on attacker actions.

Examples:

• Office spawning PowerShell
• Processes accessing LSASS memory

More resilient than tool-based detection.

---

## Level 4 – Tradecraft Detection

Detects techniques independent of tooling.

Example:

Credential dumping via LSASS memory access.

---

## Level 5 – Campaign Detection

Correlates multiple behaviors across attack stages.

Example:

Initial access → persistence → credential dumping → lateral movement.
