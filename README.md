# ROS 2 SLAM with RTAB-Map (WSL)

This project demonstrates a working SLAM pipeline using **ROS 2 Humble** and **RTAB-Map**,
running on **Ubuntu 22.04 inside WSL 2** on Windows.

The goal of this project is to show a complete, reproducible SLAM setup:
from environment installation to live visualization.

---

##  Environment

- Windows 10/11 + WSL 2 
- Ubuntu 22.04 LTS 
- ROS 2 Humble Hawksbill  
- RTAB-Map (ROS 2 packages)

---

## Running the Demo

```bash
ros2 launch rtabmap_demos robot_mapping_demo.launch.py

