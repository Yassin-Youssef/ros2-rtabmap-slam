Ubuntu 22.04 Base System Setup (WSL)

After installing Ubuntu 22.04 inside WSL 2, the system was prepared for ROS 2
and SLAM development. This step focuses on installing essential system tools
and development packages required to build and run ROS-based software.

Preparing the base system ensures that later installations (ROS 2, RTAB-Map,
and colcon builds) work reliably without missing dependencies.

Ubuntu 22.04 was used because it is the officially supported operating system
for ROS 2 Humble.

Commands Used (Ubuntu / WSL)

sudo apt update
Updates the local package list so the system is aware of the latest available
software versions.

sudo apt upgrade -y
Upgrades installed packages to their latest versions to ensure system stability
and compatibility.

sudo apt install -y build-essential
Installs the compiler toolchain (gcc, g++, make) required to build C and C++
software, including ROS packages.

sudo apt install -y cmake
Installs CMake, which is used by many ROS and C++ projects for build
configuration.

sudo apt install -y git
Installs Git, which is used for version control and managing the project
repository.

sudo apt install -y curl
Installs curl, which is used to download external resources and repository keys.

sudo apt install -y gnupg
Installs GnuPG, which is required for verifying repository signing keys.

sudo apt install -y lsb-release
Installs a tool used to detect the Ubuntu distribution version, which is
required when adding ROS repositories.

sudo apt install -y python3-pip
Installs pip for Python 3, which is used to install Python-based tools and
utilities in the ROS ecosystem.

Result

After completing this step, the Ubuntu environment contained all essential
development tools required to install ROS 2, build ROS workspaces, and run
SLAM-related software.

This step ensured that the system was fully prepared for ROS 2 Humble
installation without dependency or build issues.
