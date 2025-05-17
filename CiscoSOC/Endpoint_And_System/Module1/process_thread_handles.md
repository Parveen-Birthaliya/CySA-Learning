# Windows Architecture: Processes, Threads, and Handles

## 1. Processes

A **process** is an instance of an executing program and serves as the container for:

- Virtual address space
- Executable code
- Open handles to system objects
- Security context (access token)
- Unique Process Identifier (PID)
- Environment variables
- Priority class
- Working set size limits
- One or more threads of execution

### Characteristics of a Windows Process

| Attribute                     | Description |
|------------------------------|-------------|
| **Virtual Address Space**     | Isolated memory space assigned to the process |
| **Executable Code**           | The binary instructions that are executed |
| **Handles**                   | References to OS objects like files, registry keys, or other processes |
| **Security Context**          | Access rights and privileges via the associated token |
| **Process ID (PID)**          | Unique system-assigned identifier |
| **Priority Class**            | Base priority level (e.g., idle, normal, high) |
| **Working Set**               | Range of memory pages the process can use |
| **Threads**                   | At least one thread (the primary thread) must exist |

---

## 2. Threads

A **thread** is the fundamental unit of CPU execution within a process. Multiple threads within a process can execute concurrently and share process-wide resources.

### Thread Characteristics

| Attribute                   | Description |
|----------------------------|-------------|
| **Shared Resources**        | All threads share the process’s virtual memory and handles |
| **Thread ID (TID)**         | Unique thread identifier assigned by the system |
| **Thread Context**          | Includes CPU registers, kernel/user stacks, TEB (Thread Environment Block) |
| **Scheduling Priority**     | Determines the thread's order of execution |
| **Thread-Local Storage**    | Stores data private to the thread |
| **Exception Handlers**      | Used to handle exceptions raised during execution |
| **Security Context**        | Can impersonate other users (e.g., for remote procedure calls) |

> On startup, a process has one **primary thread**. Additional threads can be created dynamically during runtime.

---

## 3. Preemptive Multitasking

Windows employs **preemptive multitasking**, allowing the OS to allocate CPU time to threads based on priority and quantum.

- On **single-core systems**, threads are switched rapidly to simulate concurrency.
- On **multi-core systems**, threads can execute truly in parallel—one per core.

---

## 4. Handles and Objects

In Windows, a **handle** is an abstract reference to a system object. System objects include files, threads, events, processes, mutexes, and more.


## Summary

Windows abstracts program execution through the use of **processes** and **threads**, providing a controlled and secure environment for multitasking. **Threads** enable concurrent execution within processes, and **handles** provide secure access to system objects. These architectural features form the foundation for robust application behavior, system resource management, and secure interactions in modern Windows operating systems.

