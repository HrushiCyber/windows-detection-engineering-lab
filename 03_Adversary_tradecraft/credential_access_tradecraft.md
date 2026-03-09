# Credential Access Tradecraft

Credential access techniques allow attackers to obtain authentication material such as password hashes, Kerberos tickets, or plaintext credentials.

These techniques are typically executed after attackers gain an initial foothold within the environment.

---

# Common Credential Access Techniques

### LSASS Memory Dumping

The Local Security Authority Subsystem Service (LSASS) stores credential material in memory.

Attackers read LSASS memory to extract:

• NTLM hashes
• Kerberos tickets
• plaintext credentials

Common tools:

• Mimikatz
• ProcDump
• NanoDump

---

### SAM Database Dumping

The Security Account Manager (SAM) database stores local account password hashes.

Attackers may copy the SAM database and extract password hashes offline.

---

### Cached Credential Extraction

Windows stores cached domain credentials locally.

Attackers extract cached credentials from registry locations such as:

```
HKLM\Security\Cache
```

---

### DCSync Attack

Attackers impersonate a domain controller and request password hashes through the directory replication protocol.

This technique allows attackers to retrieve credentials for any domain account.
