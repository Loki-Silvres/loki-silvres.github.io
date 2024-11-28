---
layout: page
title: Hologlyph Bots
description: Swarm holonomic robots
img: assets/img/hologlyph_swarm.png
importance: 8 
category: robotics 
---

### <a href="https://github.com/Loki-Silvres/Hologlyph-Bots">[Code]</a>

This repository contains the source code and resources developed by **Team eyrc_hb_1523** for the **E-Yantra 2023-2024 Hologlyph Bots** competition. The theme focuses on leveraging **holonomic drive robots** to create artistic patterns and glyphs. With advanced motion control, the robots excel in translating complex instructions into precise drawings on a confined arena.

---
<iframe width="930" height="450" src="https://youtu.be/puT0LCRGoLM?si=_R9IvJwU_apjrbUI" title="Hologlyph Bots Demonstrations" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
---

## Project Overview

### **Key Features**
- **Holonomic Drive**: Allows for movement along X, Y, and Z (rotation) axes for precision navigation.
- **Swarm Coordination**: Multiple robots collaborating to achieve tasks efficiently.
- **Dynamic Drawing**: Capable of creating complex mathematical patterns or portraits.
- **Seamless Simulation-to-Hardware Transition**: Consistency in virtual and physical results.

---

## How the Project Was Made

### Hardware Components
- **ESP32 Microcontroller**: The brain of the robots, handling communication and motion.
- **Omnidirectional Wheels**: Facilitate smooth holonomic motion.
- **Overhead Camera System**: Provides real-time feedback for accurate localization.
- **Arena Flex-Print Surface**: A durable, custom-designed surface for glyph creation.
- **Power Supply**: Ensures stable performance for motors and microcontrollers.

### Software Components
- **ROS Humble**: Controls robot movement and handles inter-robot communication.
- **Gazebo-Classic**: Simulates tasks before real-world execution.
- **OpenCV**: Powers vision-based tasks like ArUco marker detection.
- **Python Libraries**: Used for algorithms and visualizations (`numpy`, `matplotlib`, etc.).

---

## Workflow and Implementation

### 1. **Simulation Setup**
- Design tasks in Gazebo-Classic for iterative testing and debugging.
- Implement control algorithms for holonomic movement in ROS.

### 2. **Hardware Integration**
- Transition tested simulations to the physical arena.
- Use **calibrated overhead cameras** for localization and precise task execution.

### 3. **Task Execution**
- Robots receive task-specific instructions and operate collaboratively to complete objectives.
- Artistic patterns are created using pre-planned algorithms.

---

## Task Highlights

### **Task 4: Shape Drawing**
- **Triangle and Rectangle Creation**  
  <img src="https://github.com/Loki-Silvres/Hologlyph-Bots/blob/main/Arena%20photos/task_4_triangle.png?raw=true" width="320" alt="Triangle Drawing" />
  <img src="https://github.com/Loki-Silvres/Hologlyph-Bots/blob/main/Arena%20photos/task_4_rectangle.png?raw=true" width="320" alt="Rectangle Drawing" />

---

### **Task 5: Final Arena Demonstration**
- **Arena with Robots**  
  <img src="https://github.com/Loki-Silvres/Hologlyph-Bots/blob/main/Arena%20photos/Task_5_arena_with_Bots.jpg?raw=true" width="450" alt="Arena with Bots" />

- **Final Task Output**  
  <img src="https://github.com/Loki-Silvres/Hologlyph-Bots/blob/main/Arena%20photos/Task_5_result.jpg?raw=true" width="450" alt="Final Task Result" />

---

## Repository Structure

```plaintext
Hologlyph-Bots/
├── Arduino Code/
├── Arena Photos/
├── Aruco_Markers/
├── cam_calibration_640x480/
├── hb_task1a_ws/
├── hb_task1b_ws/
├── STL files/
├── PCB and Circuit/
└── README.md
```

---

## Submission and Demonstrations
- View our complete project submissions in this [YouTube Playlist](https://youtube.com/playlist?list=PL_9--5xsFYUQ-xg70fmYQrzXn2ip_9O3C&si=z0v1tnEO03IPCXnJ).

---

## Acknowledgments
- **E-Yantra**: For fostering innovative robotics projects.