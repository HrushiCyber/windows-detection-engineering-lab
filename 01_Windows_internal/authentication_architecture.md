# Windows Authentication Architecture

Windows authentication is handled primarily by the **Local Security Authority Subsystem Service (LSASS)**.

---

# LSASS

LSASS is responsible for:

• validating logons
• managing authentication packages
• storing credential material

---

# Authentication Protocols

Windows supports multiple authentication protocols.

Examples include:

• NTLM
• Kerberos

---

# Credential Storage

Credentials may be stored in memory for active sessions.

Attackers frequently target LSASS to extract:

• NTLM hashes
• Kerberos tickets

---

# Detection Relevance

Credential dumping activities often involve:

• memory reads from LSASS
• suspicious processes accessing LSASS memory
