WSL 2 Installation and Environment Setup

This project was developed on Windows, but ROS and SLAM tools are primarily
designed to run on Linux. To avoid dual booting or using heavy virtual machines,
WSL 2 (Windows Subsystem for Linux) was chosen as the development environment.

WSL 2 provides a real Linux kernel running inside a lightweight virtualized
environment. This allows ROS 2 and RTAB-Map to run natively while remaining
fully isolated from the Windows host system.

Ubuntu 22.04 LTS was selected because it is the officially supported operating
system for ROS 2 Humble and provides stable long-term package compatibility.

Commands Used (Windows PowerShell)

wsl --status
Checks the current WSL configuration and confirms that WSL 2 is enabled.

wsl --list --online
Lists all Linux distributions available for installation using WSL.

wsl --install
Enables WSL on the system and installs the default Linux distribution using
WSL 2 as the backend.

wsl --install -d Ubuntu-22.04
Installs Ubuntu 22.04 explicitly, which is required for compatibility with
ROS 2 Humble.

Result

After running these commands, Ubuntu 22.04 was successfully installed inside
WSL 2. A Linux user account was created, and all subsequent ROS 2 and SLAM
development was performed entirely inside this Ubuntu environment.

This setup ensured that the Windows host system remained unaffected while
providing a stable and fully supported Linux environment for robotics
development.
