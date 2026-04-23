# amr_ros2_kmutnb_project

This repository provides a complete ROS2 simulation/Real environment for a differential drive mobile robot.

The system demonstrates the full robotics pipeline including:

- Gazebo simulation
- Robot modeling using URDF/Xacro
- Motor control using ros2_control
- SLAM mapping
- Localization
- Autonomous navigation using Navigation2
- Visualization using RViz

The package name used in this project is:

robot_kmutnb

---

# System Architecture

The robot system follows the pipeline below.
```bash
Navigation2
│
│ publish velocity command
▼
cmd_vel
│
▼
diff_drive_controller
│
▼
Gazebo physics simulation
│
▼
Robot movement
│
▼
Sensors (LiDAR + Odometry)
│
▼
SLAM / Localization
│
▼
Map + Robot Pose
```
---

# Package Structure

robot_kmutnb

├── config  
├── description  
├── launch  
├── meshes  
├── worlds  
├── scripts  

├── package.xml  
└── CMakeLists.txt

---

# Software Stack

This project uses the following software:

- ROS2
- Gazebo
- ros2_control
- slam_toolbox
- Navigation2
- RViz2
