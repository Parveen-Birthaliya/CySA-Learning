#  Windows Operating System Architecture: Mode-Level Breakdown

This diagram illustrates the **layered architecture** of the Windows Operating System, emphasizing the interaction between **User Mode** and **Kernel Mode** components.

![Windows OS Architecture](https://github.com/Parveen-Birthaliya/CySA-Learning/blob/main/CiscoSOC/image/win_architecture.png)

---

##  User Mode (Low Privilege)

User Mode is responsible for running applications and background services initiated by the user or system. These processes interact with the Kernel through **Kernel Interface DLLs** (e.g., `ntdll.dll`).

###  Components:
- **Non-Service Processes**: Regular user applications not running as services (e.g., `notepad.exe`)
- **Service Processes**: Background services (e.g., `svchost.exe`, antivirus)
- **User Applications**: Software like browsers, office apps, etc.
- **OS Environment Support**: Provides APIs and subsystem DLLs (e.g., Win32, POSIX, OS/2)

➡ **Kernel Interface DLLs** act as a bridge between user space and kernel space, forwarding system calls.

---

## Kernel Mode (High Privilege)

Kernel Mode has unrestricted access to hardware and system resources. It runs the core of the OS and is critical for performance, stability, and security.

###  Components:
- **Kernel Executive**: Manages high-level OS functions like memory, processes, and objects.
- **Kernel**: Low-level scheduling, synchronization, and interrupt handling.
- **Device Drivers**: Interface between hardware and the OS.
- **HAL (Hardware Abstraction Layer)**: Abstracts hardware-specific functionality to support portability across platforms.
- **Window Management and Graphics Subsystem**: Manages GUI rendering and graphical resources.

 **Security Insight**: 
- Malware attempting **privilege escalation** targets flaws in the transition from User Mode to Kernel Mode.
- **PatchGuard** and **Driver Signature Enforcement** protect Kernel Mode from unauthorized tampering.

---

##  Interaction Summary

| Component Type        | Example Process       | Role in Security Context                |
|-----------------------|------------------------|-----------------------------------------|
| User Mode App         | `calc.exe`             | Often targeted for initial access       |
| Service Process       | `svchost.exe`          | Abused for stealthy persistence         |
| Kernel Interface DLLs | `ntdll.dll`, `kernel32.dll` | Hooked by EDRs or malware for monitoring/bypass |
| Kernel Driver         | `sysmon.sys`, custom `.sys` | Target for rootkit installation         |
| HAL                   | Hardware-dependent     | Rarely attacked directly, but vital for kernel operation |

---
