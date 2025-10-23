# 🤖 Visual Servoing with BlueROV — Object Detection and PID Depth Control

> A ROS2-based project integrating computer vision and real-time control for the **BlueROV** underwater robot.  
> The robot autonomously detects and follows a target object using visual feedback and PID-based depth control.  
> Conducted as part of the *Marine Mechatronics and Visual Servoing* course in the **Erasmus Mundus MIR Programme** at Université de Toulon.

---

## 🌊 Overview

This project focuses on developing a **visual servoing system** for an underwater robot using ROS2 and Python.  
The main goal was to enable the BlueROV to **detect and track a colored object** while maintaining a desired depth using real-time camera feedback and PID control.

The work was divided into two main parts:
1. **Object Detection and Tracking** – Using color segmentation to detect an orange buoy or ArUco markers.  
2. **Visual Servoing and Depth Control** – Implementing proportional and PID controllers to keep the robot centered and stable underwater.

---

## 📂 Repository Structure

| Path | Description |
|------|--------------|
| **Assignment_Explanation/** | Notes, calibration data, and setup instructions for experiments |
| **Codes/** | Source code for vision processing and control implementation |
| ├── `image_processing_mir.py` | Detects objects using HSV color thresholding and publishes coordinates |
| ├── `listenerMIR.py` | Performs visual servoing control based on object position feedback |
| ├── `camera_parameters.py` | Contains HSV ranges and calibration parameters |
| └── `launch/` | ROS2 launch files to run multiple nodes together |
| **BlueROV_Detecting_Object_Report.pdf** | Practical 1 – Object detection and tracking experiments |
| **Visual_Servoing_PID_control_report.pdf** | Practical 2 – Visual servoing and depth PID control analysis |
| **README.md** | Project documentation (this file) |

---

## 🎯 Project Objectives

- Develop a robust **object detection** system using color-based segmentation.  
- Implement a **visual servoing controller** that reacts to the target’s position in real time.  
- Design a **PID depth controller** to stabilize vertical movement of the ROV.  
- Integrate vision and control under a single **ROS2 framework** for modular operation.  

---

## ⚙️ Implementation Summary

### Object Detection and Tracking
- Used OpenCV to convert RGB images into HSV space for color-based segmentation.  
- Detected an orange buoy and published its coordinates and size to a ROS2 topic.  
- Improved detection stability by tuning HSV thresholds and removing background noise.  
- Verified detection accuracy under different lighting and water conditions.

### Visual Servoing Control
- Implemented a proportional control system reacting to the object’s position in the camera frame.  
- Controlled yaw, pitch, and forward motion to align the robot with the target.  
- The ROV performed smooth tracking with reduced oscillations after fine-tuning control gains.  

### Depth PID Control
- Added a separate PID controller to maintain a constant underwater depth.  
- Compensated buoyancy effects by adjusting the integral term.  
- Tested stability at different depth setpoints and validated consistent convergence.  

---

## 🧠 Results and Observations

| Objective | Result |
|------------|---------|
| Object detection | 90% stable tracking in variable lighting |
| Visual servoing | Smooth alignment and accurate centering |
| Depth control | ±0.05 m precision after PID tuning |
| Integration | Fully operational under ROS2 with live feedback |

---

## 🧩 Tools & Technologies

- **ROS2 (rclpy)** – Node management, topics, and message handling  
- **Python / OpenCV** – Image processing and color segmentation  
- **PlotJuggler** – Real-time control data visualization  
- **BlueROV2** – Underwater robotic platform  
- **PID Control** – Depth stabilization and motion control  

---

## 🧠 Key Learning Outcomes

| Area | What I Learned |
|------|----------------|
| Computer Vision | Real-time object detection and HSV tuning |
| Visual Servoing | Translating image feedback into motion control |
| PID Tuning | Balancing responsiveness and stability underwater |
| ROS2 Framework | Designing modular nodes for control and perception |
| System Integration | Combining multiple subsystems into a single pipeline |

---

## 👩‍🔬 Authors

**Hyejoo Kwon**, Sahil Abdullayev, Samantha Connolly, Alexander Endresen  
📍 *Erasmus Mundus Master’s in Marine & Maritime Intelligent Robotics (MIR)*  
🧑‍🏫 *Instructors:* Prof. Vincent Hugel & Prof. Vincent Creuze  
📅 Submitted: March 2025  

🔗 [GitHub Repository](https://github.com/S1194789/Visual-Servoing-with-BlueROV)
