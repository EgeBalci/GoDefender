# Go Defender

![Go Defender](GoDefender.png)

## Anti-Malware Go Package

This Go package provides functionality to detect and defend against various forms of malware, including debugging tools, virtualization environments, and critical processes.

### Anti-Virtualization

This module contains functions to detect virtualization environments commonly used for malware analysis and evasion.

- **Triage Detection**: Detects if the system is running in a triage or analysis environment.
- **Monitor Metrics**: Monitors system metrics to identify abnormal behavior indicative of virtualization.
- **VirtualBox Detection**: Detects the presence of Oracle VirtualBox.
- **VMWare Detection**: Detects the presence of VMware virtualization software.
- **KVM Check**: Checks for Kernel-based Virtual Machine (KVM) hypervisor.
- **Username Check**: Verifies if the current user is a default virtualization user.

### Anti-Debug

This module includes functions to detect and prevent debugging and analysis of the running process.

- **IsDebuggerPresent**: Checks if a debugger is currently attached to the process.
- **Remote Debugger**: Detects if a remote debugger is connected to the process.
- **PC Uptime**: Monitors system uptime to detect debugging attempts based on system restarts.
- **Check Blacklisted Windows Names**: Verifies if the process name matches any blacklisted names commonly used by debuggers.
- **Running Processes**: Retrieves a list of running processes and identifies potential malicious ones.
- **Parent Anti-Debug**: Detects if the parent process is attempting to debug the current process.
- **Kill Bad Processes**: Terminates known malicious processes detected on the system.

### Process

This module focuses on critical processes that should be monitored or protected.

- **Critical Process**: Implements functionality to manage critical processes essential for system operation.
