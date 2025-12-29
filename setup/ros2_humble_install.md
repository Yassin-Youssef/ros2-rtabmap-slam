ROS 2 Humble Installation (Ubuntu 22.04)

ROS 2 Humble Hawksbill was installed as the main robotics middleware for this project.
ROS 2 provides the communication framework, tools, and runtime support required for SLAM systems such as RTAB-Map.

Humble was selected because it is the long-term supported (LTS) ROS 2 distribution officially compatible with Ubuntu 22.04, ensuring stability and package compatibility.

ROS 2 was installed using the official ROS package repositories.

Installation

The full desktop version of ROS 2 Humble was installed. This includes core ROS libraries, command-line tools, and visualization tools such as RViz.

sudo apt update
sudo apt install -y ros-humble-desktop

Environment Setup

The ROS 2 environment was sourced to make ROS commands available in the current terminal session.

source /opt/ros/humble/setup.bash

To make this change persistent across new terminal sessions, the setup command was added to the shell configuration file.

echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
source ~/.bashrc

Verification

The installation was verified by checking the active ROS distribution and ensuring ROS 2 commands were available.

echo $ROS_DISTRO
ros2 --version
ros2 pkg list | head
