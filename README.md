# MathWorks Mini Drone Competition 2024: Team Drone Landers

Welcome to the repository for **Team Drone Landers**, participants in the MathWorks Mini Drone Competition 2024. Our project focuses on the development of an autonomous minidrone using **Model-Based Design (MBD)** in Simulink to perform complex line-following tasks. Below, you'll find all the essential details of our project.

---

## Team Members
- **Parthibanraj P** (23BMC070)
- **Gopinath Pandian N** (23BMC016)
- **Manikandan M** (23BCS082)
- **Pradeepraaj S** (23BEC128)

### Institution
**Kumaraguru College of Technology**  
Chinnavedampatti, Coimbatore - 641049.

**Faculty Advisor:**  
Dr. J. Darshan Kumar  
Assistant Professor, Aeronautical Engineering  

---

## Problem Statement
Develop an autonomous minidrone capable of following a black line on a white background with precision. The drone must maintain a stable trajectory, navigate through complex line configurations, and avoid obstacles. The project leverages **Simulink** for algorithm development, simulation, and hardware integration.

---

## Abstract
This project focuses on creating an autonomous minidrone equipped with a robust line-following algorithm. Using **image processing**, **state estimation**, and **control strategies**, the drone can navigate autonomously while maintaining stability. The project highlights the use of **Model-Based Design (MBD)** for rapid prototyping and efficient testing.

---

## Introduction
Autonomous drones are revolutionizing various industries such as agriculture, surveillance, and disaster management. This project explores the fundamental task of line following, implemented on a Parrot Mambo Minidrone using Simulink. The drone employs real-time image processing and control systems for navigation and obstacle avoidance.

---

## Competition Overview
The MathWorks Mini Drone Competition introduces participants to **Model-Based Design** using Simulink.  

### Rounds:
1. **Simulation Round:** Teams design and refine their minidrone algorithms in Simulink.  
2. **Simulation and Hardware Deployment Round:** Qualified teams deploy their models on Parrot Mambo Minidrone hardware using the Simulink Support Package.

---

## Technical Details

### Configuration
- **Software Used:** MATLAB Simulink  
- **Hardware Platform:** Parrot Mambo Minidrone  
- **Control System:** PID-based position and orientation control  
- **Key Functionalities:**  
  - Line detection using image processing  
  - Stable trajectory maintenance  
  - Autonomous decision-making  

---

### Flight Controller System
The flight control system is responsible for:  
- **Attitude Control:** Maintaining drone orientation.  
- **Position Control:** Ensuring accurate movement along the path.  
- **Obstacle Avoidance:** Preventing collisions using sensors.  
- **Mission Execution:** Following predefined flight paths autonomously.  

---

### Image Processing System
The image processing subsystem includes:  
1. **Image Acquisition:** Captures real-time RGB frames from the drone's camera.  
2. **Image Conversion:** Converts images into analyzable formats.  
3. **Feature Extraction:** Identifies line boundaries using Canny filters and Hough transform.  
4. **Decision Logic:** Determines navigation adjustments based on detected features.  

---

## Line Following Algorithm
The drone uses a dual-strategy approach for line tracking:  
1. **Hough Line Transform:** Detects edges and calculates a central path for the drone.  
2. **Region of Interest (ROI):** Identifies intersections of the line with predefined ROI for stable heading adjustments.  

A separate function identifies circular markers for precise landing, ensuring that the drone only lands when aligned correctly.

---

## Simulation
Simulink-based simulation validates the drone's performance in a controlled environment. Key features include:  
- Real-time image processing  
- Trajectory stability tests  
- Fine-tuning control parameters  

---

## Arena Details
The competition arena consists of:  
- Black line on a white surface for navigation  
- Circular markers for landing zones  
- Potential obstacles for avoidance  

---

## Results
The project successfully demonstrated:  
- Accurate line tracking using advanced image processing.  
- Stable trajectory even in complex configurations.  
- Effective landing mechanisms in designated areas.  

---

## Conclusion
This project showcased the potential of Model-Based Design for autonomous drone development. The use of Simulink enabled rapid prototyping, effective simulation, and successful deployment on hardware. This approach can be extended to other autonomous drone applications.

---

## References
1. MathWorks Documentation: [Simulink for Minidrones](https://www.mathworks.com/products/simulink.html)  
2. Parrot Mambo Minidrone Support Package: [MathWorks Support](https://www.mathworks.com/hardware-support/parrot.html)  
3. Image Processing Toolbox: [MathWorks Documentation](https://www.mathworks.com/products/image.html)  

---

Developed by **[max-mani](https://github.com/max-mani)** and Team Drone Landers.
