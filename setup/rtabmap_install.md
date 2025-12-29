RTAB-Map Setup and SLAM Execution (ROS 2 Humble)

RTAB-Map (Real-Time Appearance-Based Mapping) was used in this project as the
SLAM backend. RTAB-Map provides graph-based SLAM capabilities and integrates
directly with ROS 2 through the rtabmap_ros package stack.

Instead of building RTAB-Map from source, the ROS 2 packages provided through
the official ROS repositories were used. This approach reduces build complexity
and ensures compatibility with ROS 2 Humble on Ubuntu 22.04.

RTAB-Map ROS Packages

After installing ROS 2 Humble, RTAB-Map-related ROS packages became available
as part of the ROS ecosystem. These packages include:

rtabmap_ros
Provides the core ROS 2 integration for RTAB-Map, including SLAM nodes and
parameters.

rtabmap_demos
Provides example launch files and demo configurations used to verify correct
installation and functionality.

rtabmap_viz
Provides visualization tools for RTAB-Map, including the graphical interface
used to display mapping results.

rtabmap_sync
Provides sensor synchronization utilities required for SLAM pipelines.

Commands Used (Ubuntu / WSL)

ros2 pkg list | grep rtabmap
Lists all installed RTAB-Map-related ROS 2 packages to verify availability.

ls /opt/ros/humble/share/rtabmap_demos/launch
Lists available RTAB-Map demo launch files to identify the correct launch
configuration.

ros2 launch rtabmap_demos robot_mapping_demo.launch.py
Launches an official RTAB-Map demo that starts sensor synchronization, visual
odometry, the SLAM backend, and the RTAB-Map visualization interface.

Result

After running the demo launch file, the RTAB-Map graphical interface opened
successfully. ROS 2 nodes started without errors, and terminal output confirmed
that the SLAM pipeline was running.

The visualization window displayed a 3D scene with coordinate axes, confirming
that RTAB-Map and its visualization tools were functioning correctly. Screenshots
of the running system were captured and stored in the results/ directory as
proof of successful SLAM execution.
