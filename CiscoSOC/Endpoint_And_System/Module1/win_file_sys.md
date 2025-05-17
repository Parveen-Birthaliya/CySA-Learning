# Windows File System Structure and NTFS Alternate Data Streams (ADS)

## Section 1: Windows File System Structure

In a Windows environment, **every connected storage device** maintains its own file system. The **Windows OS is typically installed** on the **first physical hard disk**, which is assigned the **drive letter `C:`**. Drive letter assignment continues alphabetically with additional devices. The file system is **case-insensitive by default**, meaning `C:\` and `c:\` point to the same location.

![Windows File Architecture](https://github.com/Parveen-Birthaliya/CySA-Learning/blob/main/CiscoSOC/image/win_file_sys.png)
### Primary Directories in the Windows File System

| Directory             | Purpose                                                                                      |
|-----------------------|-----------------------------------------------------------------------------------------------|
| **Boot**              | Hidden directory containing system boot files.                                               |
| **Logs**              | (Windows 10+) Stores Windows event logs.                                                     |
| **PerfLogs**          | Stores performance logs (if performance monitoring is enabled).                              |
| **Program Files**     | Stores 64-bit application files (on 64-bit systems).                                         |
| **Program Files (x86)** | Stores 32-bit application files (on 64-bit systems).                                        |
| **ProgramData**       | Application data directory. Apps use subdirectories for storing shared configuration data.   |
| **Users**             | Root directory for all user profiles and personal data.                                      |
| **Public**            | Subdirectory of `Users`; shared among all user accounts.                                     |
| `<username>`          | Individual user directories under `Users\`. Contains personal documents, downloads, etc.     |
| `AppData`             | Subfolder under each user's directory for storing user-specific app data (e.g., browser history). |
| **Windows**           | Contains core OS files and system subsystems.                                                |
| **System**            | (Legacy) Used for 16-bit DLLs; mostly empty on 64-bit systems.                               |
| **System32**          | Stores 64-bit system DLLs and essential binaries.                                            |
| **SysWOW64**          | Holds 32-bit DLLs on 64-bit systems to support backward compatibility.                       |
| **WinSxS**            | "Windows Side-by-Side" — maintains multiple DLL versions for compatibility with legacy apps. |

---
