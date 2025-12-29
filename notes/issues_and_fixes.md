Issues Encountered and Fixes

This file documents the main issues encountered during the setup and execution
of the ROS 2 SLAM pipeline, along with how each issue was diagnosed and resolved.
These problems reflect real-world setup challenges and the debugging process
used to overcome them.

WSL and Linux Environment Confusion

Issue:
Initially, it was unclear whether WSL behaves like a virtual machine or directly
affects the Windows system. There was concern about system safety and whether
installing ROS would impact Windows.

Fix:
It was confirmed that WSL 2 runs a real Linux kernel inside an isolated virtual
environment. All ROS and SLAM-related installations occur entirely inside the
Ubuntu subsystem and do not modify the Windows host system. This allowed safe
development without dual booting or traditional virtual machines.

Package Not Found: python3-colcon-common-extensions

Issue:
When attempting to build a ROS 2 workspace, the colcon command was not found.
An initial attempt to install python3-colcon-common-extensions failed with
a “package not found” error.

Fix:
The issue was caused by attempting to install ROS-related tools before adding
the ROS 2 repositories. After properly adding the ROS 2 apt repository and
installing ROS 2 Humble, the python3-colcon-common-extensions package became
available and was installed successfully. The colcon build tool then worked
as expected.

colcon Build Shows Zero Packages

Issue:
Running colcon build returned a summary indicating that zero packages were
built, which initially seemed like an error.

Fix:
This behavior was identified as normal because the workspace did not yet contain
any ROS packages. The output confirmed that colcon was installed and functioning
correctly.

RTAB-Map Launch File Not Found

Issue:
An attempt was made to launch the RTAB-Map demo using an incorrect launch file
name, resulting in a “file not found” error.

Fix:
The available launch files were inspected by listing the contents of the
rtabmap_demos/launch directory. This revealed the correct launch file name,
robot_mapping_demo.launch.py, which was then used successfully.

RTAB-Map GUI and Visualization Verification

Issue:
There was uncertainty about whether RTAB-Map was actually running correctly,
as the initial visualization showed only coordinate axes without a map.

Fix:
It was confirmed that this behavior is expected for the demo configuration.
The successful launch of ROS 2 nodes, terminal log output, and the RTAB-Map GUI
window together confirmed that the SLAM pipeline was running. Screenshots were
captured as visual proof.

WSL File Access and Screenshot Management

Issue:
There was confusion about how to move screenshots from the Windows desktop into
the WSL project directory.

Fix:
WSL’s integration with Windows file paths was used to access the Linux filesystem
from Windows Explorer. Screenshots were manually placed into the results/
directory to keep all project artifacts organized within the repository.

Summary

All encountered issues were related to environment setup, package availability,
or command usage. Each issue was resolved through inspection, verification, and
incremental troubleshooting. This process ensured a stable ROS 2 Humble and
RTAB-Map setup suitable for SLAM demonstrations and documentation
