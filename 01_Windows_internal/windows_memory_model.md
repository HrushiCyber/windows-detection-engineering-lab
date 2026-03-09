# Windows Memory Model

Windows uses a virtual memory architecture.

Each process operates within its own **virtual address space**.

---

# Virtual Memory

Virtual memory abstracts physical memory.

Each process receives a private address space that maps to physical memory.

---

# Memory Regions

Common memory regions include:

• code segments
• heap memory
• stack memory

---

# Memory Protection

Windows enforces memory protections such as:

• read
• write
• execute

Attackers often bypass these protections through **memory injection techniques**.

---

# Detection Relevance

Memory manipulation behaviors can indicate:

• process injection
• shellcode execution
• credential dumping
