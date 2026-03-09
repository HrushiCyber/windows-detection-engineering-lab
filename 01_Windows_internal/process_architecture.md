# Windows Process Architecture

Understanding the Windows process model is fundamental for endpoint detection engineering.

---

# What Is a Process

A process is an instance of a program in execution.

Each process includes:

• virtual address space
• execution threads
• security token
• open handles to system objects

Processes are managed by the **Windows kernel**.

---

# Process Components

Key components of a Windows process include:

### Virtual Address Space

Each process receives its own virtual memory space.

This isolates processes from each other.

---

### Threads

Threads are execution units within a process.

A process can contain multiple threads.

---

### Security Token

The security token defines the privileges and identity of the process.

It contains:

• user SID
• group memberships
• privileges

Attackers frequently attempt to **steal or manipulate tokens**.

---

# Parent-Child Process Relationships

Windows maintains process lineage through **parent process IDs**.

Example chain:

```
explorer.exe
   └── powershell.exe
         └── rundll32.exe
```

Detection engineers analyze process trees to detect suspicious execution chains.

---

# Detection Relevance

Suspicious parent-child relationships often indicate malicious activity.

Examples include:

• Office applications spawning PowerShell
• browsers spawning command shells
• script interpreters launching system binaries
