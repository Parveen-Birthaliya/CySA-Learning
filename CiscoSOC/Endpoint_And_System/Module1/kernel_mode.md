# Windows OS Architecture: Kernel Mode

## Overview

Kernel mode is the privileged execution environment in the Windows operating system where core system components operate. Unlike user mode, where each process runs in a separate, protected memory space, kernel mode processes share a common memory space. This design provides higher speed and direct access to system resources—but also introduces risks.

To reduce the risk of system compromise or instability, **Windows enforces Kernel Mode Code Signing (KMCS)**. This requires all kernel-mode components (e.g., drivers) to be digitally signed by a trusted Certificate Authority.

## Key Components of Kernel Mode

### 1. Kernel Executive

Provides foundational OS services such as:

- Input/Output (I/O) operations
- Memory management
- Object management
- Networking
- Process and thread management

### 2. Kernel

Handles core low-level system tasks including:

- **Thread scheduling**
- **System interrupt handling**
- **Context switching**

This component ensures real-time responsiveness and multitasking at the CPU level.

### 3. Device Drivers

Serve as an interface between hardware and the OS. Drivers handle:

- I/O communication
- Interrupt handling
- Direct Memory Access (DMA)

Drivers must be signed to prevent rootkit injections and unauthorized access to kernel memory.

### 4. Hardware Abstraction Layer (HAL)

Abstracts hardware differences (e.g., chipsets, motherboards) by translating hardware-level instructions into standardized OS-level calls.

Benefits:
- Platform independence
- Simplified hardware interfacing
- Facilitates portability and hardware compatibility

### 5. Window Management and Graphics Subsystem

Handles:

- Graphical User Interface (GUI) rendering
- Screen drawing
- Input device interpretation (keyboard, mouse)

This subsystem ensures smooth user interaction with the graphical shell.

---

## Core Executable and DLLs in Kernel Mode

| Component       | Description |
|----------------|-------------|
| **`ntoskrnl.exe`** | Windows NT kernel and executive (core component) |
| **`hal.dll`**      | Hardware Abstraction Layer module |
| **`win32k.sys`**   | Kernel-mode driver for window management, input handling, and display |
| **`ntdll.dll`**    | Interface between user mode and kernel mode; handles system calls |
| **`kernel32.dll`** | Core Windows API; base layer for memory, threads, I/O |
| **`advapi32.dll`** | Provides registry, service, and security-related functions |
| **`user32.dll`**   | User interface management: windows, menus, dialog boxes |
| **`gdi32.dll`**    | Graphics Device Interface (GDI); responsible for drawing graphics and text |

---
