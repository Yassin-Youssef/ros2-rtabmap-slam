All Commands Used in the Project

This file contains a complete list of commands used throughout the project,
in chronological order, with a short explanation for each command.
All commands were executed either in Windows PowerShell or inside the Ubuntu
22.04 environment running in WSL 2.

Windows (PowerShell) Commands

wsl --status
Checks the current WSL configuration and default version.

wsl --list --online
Lists all available Linux distributions that can be installed using WSL.

wsl --install
Enables WSL and installs the default Linux distribution using WSL 2.

wsl --install -d Ubuntu-22.04
Installs Ubuntu 22.04 explicitly, which is required for ROS 2 Humble.

Ubuntu / WSL Commands

sudo apt update
Updates the local package list from Ubuntu repositories.

sudo apt install -y curl gnupg lsb-release
Installs tools required to add external repositories securely.

sudo mkdir -p /etc/apt/keyrings
Creates a directory to store repository signing keys.

curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.key
 | sudo tee /etc/apt/keyrings/ros-archive-keyring.gpg
Adds the official ROS 2 GPG signing key.

echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu
 $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/ros2.list
Adds the ROS 2 package repository to the system.

sudo apt update
Refreshes package lists after adding the ROS 2 repository.

sudo apt install -y ros-humble-desktop
Installs ROS 2 Humble Desktop, including RViz and core ROS tools.

source /opt/ros/humble/setup.bash
Loads the ROS 2 environment into the current terminal session.

echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
Ensures ROS 2 is sourced automatically in every new terminal.

source ~/.bashrc
Applies the updated shell configuration.

sudo apt install -y python3-colcon-common-extensions
Installs the colcon build tool used for ROS 2 workspaces.

colcon build
Builds packages in the current ROS 2 workspace.

ros2 pkg list | grep rtabmap
Lists installed RTAB-Map-related ROS 2 packages.

ls /opt/ros/humble/share/rtabmap_demos/launch
Lists available RTAB-Map demo launch files.

ros2 launch rtabmap_demos robot_mapping_demo.launch.py
Launches the RTAB-Map SLAM demo with visualization.

End of Command List
