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
