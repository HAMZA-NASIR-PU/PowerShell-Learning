# PowerShell Learning 🚀

Welcome to my PowerShell Learning repository! This is a space dedicated to mastering Windows PowerShell from scratch. Whether you're a beginner or looking to deepen your understanding, this repo covers everything from the fundamentals to advanced scripting techniques.

🔧 **What you'll find here**:
- **Basic Commands**: Learn the most common PowerShell commands.
- **Scripting**: Understand how to write efficient PowerShell scripts.
- **Automation**: Explore how to automate repetitive tasks using PowerShell.
- **Advanced Topics**: Dive into modules, functions, and error handling.

💻 **Technologies Used**:
- **PowerShell** 🖥️
- **Windows OS** 🖱️

📚 **Why PowerShell?**:
PowerShell is an essential skill for Windows users, system administrators, and developers alike. It allows you to automate tasks, manage configurations, and streamline workflows efficiently.

🔗 **Links**:
- [Official PowerShell Documentation](https://docs.microsoft.com/en-us/powershell/)
- [PowerShell on GitHub](https://github.com/PowerShell/PowerShell)

---

## **🔍 Windows Management Instrumentation (WMI) classes**

**Windows Management Instrumentation (WMI) classes** are part of the **WMI infrastructure**, which allows you to manage and interact with the underlying Windows operating system. These classes represent various components of a Windows system, such as hardware, system configuration, services, processes, network settings, and more.

---

### 🔍 What Exactly Are WMI Classes?

WMI classes are similar to object-oriented programming classes. They describe properties and methods of system resources. You can query, monitor, and control these resources using tools like **PowerShell**, **WMIC**, **VBScript**, or **C#** via .NET.

---

### ✅ Example Use Cases

| Task                        | WMI Class Involved              |
|----------------------------|----------------------------------|
| Get OS details             | `Win32_OperatingSystem`         |
| List running processes     | `Win32_Process`                 |
| Get CPU information        | `Win32_Processor`               |
| Find disk space info       | `Win32_LogicalDisk`             |
| Get network adapter config | `Win32_NetworkAdapterConfiguration` |

---

### 💡 Example (PowerShell)

```powershell
Get-WmiObject -Class Win32_OperatingSystem
```

This retrieves information like OS name, version, build number, free physical memory, etc.

---

### 🧠 Key Concepts

- **Namespace**: WMI classes are grouped in namespaces. Most common: `root\CIMV2`
- **Inheritance**: WMI classes are based on the **CIM (Common Information Model)** schema.
- **Access**: You can access WMI remotely for system management tasks.

---

## **🧾 WMI Classes Cheat Sheet**

| 🎯 Purpose                        | 🧱 WMI Class                              | 🔎 Description |
|----------------------------------|-------------------------------------------|----------------|
| OS Info                          | `Win32_OperatingSystem`                   | OS version, build, architecture, memory |
| Processor Info                   | `Win32_Processor`                         | CPU name, cores, load, speed |
| BIOS Info                        | `Win32_BIOS`                              | BIOS version, manufacturer |
| Motherboard Info                 | `Win32_BaseBoard`                         | Motherboard model, manufacturer |
| RAM Info                         | `Win32_PhysicalMemory`                    | Installed RAM details |
| Disk Drive Info                  | `Win32_DiskDrive`                         | Hard drives and SSDs |
| Logical Disk (C:, D:) Info       | `Win32_LogicalDisk`                       | Drive letter, space used, free space |
| Partition Info                   | `Win32_DiskPartition`                     | Partition size, type |
| Network Adapter Info             | `Win32_NetworkAdapter`                    | NIC name, status |
| Network Config Info              | `Win32_NetworkAdapterConfiguration`       | IP, MAC, DNS settings |
| Installed Software               | `Win32_Product`                           | Installed apps (⚠️ slow & heavy) |
| Services                         | `Win32_Service`                           | List and control services |
| Running Processes                | `Win32_Process`                           | List of active processes |
| Startup Programs                 | `Win32_StartupCommand`                    | Programs set to auto-start |
| Battery Info (Laptops)           | `Win32_Battery`                           | Battery status and capacity |
| User Accounts                    | `Win32_UserAccount`                       | List of local users |
| Logged-in Users                  | `Win32_ComputerSystem`                    | Includes username |
| System Boot Time                 | `Win32_OperatingSystem`                   | Look at `LastBootUpTime` |

---

## ⚙️ **PowerShell Example Commands**

```powershell
# Get OS Info
Get-WmiObject -Class Win32_OperatingSystem

# Get CPU Info
Get-WmiObject -Class Win32_Processor

# Get Logical Drives
Get-WmiObject -Class Win32_LogicalDisk

# List Running Processes
Get-WmiObject -Class Win32_Process | Select-Object Name, ProcessId

# Get Installed Physical RAM
Get-WmiObject -Class Win32_PhysicalMemory
```

---

## 🚀 Tips

- Use `Get-WmiObject` or the newer `Get-CimInstance` in PowerShell 5+.
- Use `Select-Object *` to see all properties.
- Use filtering to narrow down results:
  ```powershell
  Get-WmiObject -Class Win32_Service -Filter "State='Running'"
  ```

---

