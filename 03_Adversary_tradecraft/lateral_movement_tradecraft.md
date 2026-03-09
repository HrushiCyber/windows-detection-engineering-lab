# Lateral Movement Tradecraft

Lateral movement techniques allow attackers to expand their access across the network.

After gaining access to one host, attackers attempt to move to additional systems.

---

# Common Lateral Movement Techniques

### PsExec

PsExec allows remote command execution via SMB.

Attackers frequently use it to execute commands on remote systems.

---

### Windows Management Instrumentation (WMI)

WMI enables remote command execution and system management.

Attackers use WMI to execute commands without dropping files on disk.

---

### SMB Admin Shares

Administrative shares such as `ADMIN$` allow attackers to copy tools between systems.

---

### Remote Service Creation

Attackers create services remotely to execute payloads on target systems.
