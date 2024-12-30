# MathWorks Minidrone Competition 2024  
**Team Name:** Drone Landers  

Welcome to our project repository for the MathWorks Minidrone Competition 2024! This repository contains all the essential information, models, and algorithms used for developing our autonomous minidrone capable of line-following.  

---

## Problem Statement  
Develop an autonomous minidrone capable of accurately following a black line on a white background. The drone should maintain a stable trajectory while navigating through various line configurations and obstacles using Model-Based Design (MBD) in Simulink for algorithm development, simulation, and hardware integration.  

---

## Abstract  
This project demonstrates the development of an autonomous line-following minidrone using Model-Based Design. Key elements include image processing for line detection, state estimation for position and orientation tracking, and robust control strategies for maintaining stable trajectories. Using Simulink, the line-following algorithm was designed, simulated, and successfully tested in hardware.  

**Keywords:** Autonomous minidrone, Line following, Simulink, Image processing, Algorithm development.  

---

## Line Following Algorithm  

### **Overview**  
The line-following algorithm is the heart of this project, enabling the drone to detect and follow a line with precision. Using advanced image processing techniques and control systems, the algorithm ensures smooth navigation along the designated path.  

---

### **Algorithm Implementation Steps**  

1. **Image Processing**  
   - **Image Acquisition:** Captures live feed from the minidrone's onboard camera.  
   - **RGB Channel Separation:** Splits the image into Red, Green, and Blue channels for processing.  
   - **Canny Edge Detection:** Identifies edges in the image, focusing on the black line.  
   - **Hough Line Transform:** Detects and extracts the line's orientation by finding its boundaries.  

2. **Heading Calculation**  
   - The algorithm computes the line's central axis using the first two lines from the Hough Transform.  
   - Averages coordinates to generate a guiding line.  
   - Corrects heading errors to maintain stability along the path.  

3. **Advanced ROI Method**  
   - Regions of Interest (ROIs) are defined to filter out irrelevant line segments.  
   - The drone adjusts its orientation based on line intersection within these ROIs.  
   - Past heading information is utilized to enhance decision-making, especially in scenarios involving sharp turns or complex paths.  

4. **Circle Detection and Landing**  
   - At the end of the line, the drone detects a circular marker using the `imfindcircles()` function.  
   - The drone identifies the center of the circle and aligns its position.  
   - Landing is executed only when the circle is fully within the ROI to avoid false positives.  

---

### **Algorithm Insights**  
#### First Method: Centralized Mean Line Calculation  
- Utilizes two primary lines detected by the Hough Transform.  
- Finds the mean of the two lines for determining the central path.  
- Works well for straight-line paths but has limitations during sharp turns.  

#### Second Method: Enhanced ROI-Based Heading  
- Overcomes the limitations of the first method by dynamically adjusting ROIs.  
- Leverages bitmap data of the detected line to evaluate the region overlap.  
- Provides improved heading stability and adaptability in challenging conditions.  

#### Circle Detection for Landing  
- Incorporates MATLAB's built-in `imfindcircles()` for accurate circle identification.  
- Combines circle detection with ROI validation for safe and precise landings.  

---

## Key Features  
- Robust PID control ensures smooth and stable movement.  
- High-performance image processing allows accurate line detection in real time.  
- Dynamic obstacle avoidance incorporated through visual data.  

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

## Flight Controller System  
The flight control system is the backbone of the minidrone's operation, encompassing the following:  
- **Attitude Control:** Maintains orientation stability.  
- **Position Control:** Keeps the drone on the desired path.  
- **Mission Execution:** Accomplishes pre-programmed tasks, including landing.  

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

## How to Run  
1. Clone the repository to your local machine.  
   ```bash
   git clone https://github.com/max-mani/MinidroneCompetition.git  
   cd MinidroneCompetition  

---

Developed by **[max-mani](https://github.com/max-mani)** and Team Drone Landers.
