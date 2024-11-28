---
layout: page  
title: Hologlyph Bots  
description: Swarm Holonomic Robots for Autonomous drawing
img: assets/img/hologlyph_swarm.png  
importance: 2 
category: robotics  
---

### <a href="https://github.com/Loki-Silvres/Hologlyph-Bots">[Code]</a>  

This project builds on the concepts developed for the **E-Yantra 2023-2024 Hologlyph Bots** competition, transforming it into a comprehensive **DIY package** for creating swarm holonomic robots. These robots excel in precise movement and collaborative tasks, enabling them to draw artistic patterns, glyphs, or mathematical shapes in a confined arena. This repository includes detailed instructions for both simulation and hardware implementation, making it an excellent starting point for enthusiasts, researchers, and hobbyists.  

---
<iframe width="930" height="450" src="https://www.youtube.com/embed/puT0LCRGoLM" title="Hologlyph Bots Demonstrations" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
---  

## Project Overview  

### **Key Features**  
- **Holonomic Drive**: Move seamlessly in X, Y, and rotational (Z) axes for precision.  
- **Swarm Robotics**: Coordinate multiple robots to achieve complex tasks collaboratively.  
- **Patterns**: Generate shapes, glyphs, and even portraits dynamically.  
- **DIY-Friendly Package**: Includes simulation models, hardware assembly guides, and complete ROS-based control instructions. 

---

## How the Project Was Made  

### Hardware Components  
- **ESP32 Microcontroller**: Handles robot control and communication.  
- **Omnidirectional Wheels**: Enables smooth holonomic motion.  
- **Overhead Camera System**: For precise localization and feedback.  
- **Arena Flex-Print Surface**: Durable and customizable drawing surface.  
- **3D-Printed Components**: Simplifies hardware assembly using STL files.  

### Software Components  
- **ROS Humble**: Controls robot movement and facilitates swarm communication.  
- **Gazebo-Classic**: Simulates tasks for testing and refining control strategies.  
- **OpenCV**: Powers vision-based localization using ArUco markers.  
- **Python Libraries**: For control algorithms, visualizations, and debugging.  

---

## Workflow and DIY Instructions  

### 1. **Simulation Setup**  
- Start with the provided **Gazebo simulation files** to test robot movement and control strategies.  
- Experiment with the integrated control algorithms for holonomic motion.  

### 2. **Hardware Assembly**  
- Use the provided STL files to 3D print components for the robots.  
- Assemble robots following detailed instructions, and wire components including **ESP32** and motors.  

### 3. **Task Execution**  
- Calibrate the overhead camera system for precise localization.  
- Upload pre-programmed control scripts to the ESP32 for artistic pattern generation.  

### 4. **Swarm Coordination**  
- Test multi-robot coordination using the included ROS launch files.  
- Program custom patterns or import your designs to draw collaboratively.  

---

## Results and Highlights

### **Shape Drawing**  

<div class="row">
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/holo_shapes_sim.png" title="simulation image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/task_4_triangle.png" title="triangle image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/task_4_rectangle.png" title="rectangle image" class="img-fluid rounded z-depth-1" %}
    </div> 
</div>
<div class="caption">
    On the left, Simulation shapes. Middle, Physically drawn triangle. Right, Physically drawn rectangle.
</div>

---

### **Arena with Robots**  
<div class="row">
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/transformed_arena.png" title="simulation image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-4 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Task_5_arena_with_Bots.png" title="triangle image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    On the left, Perspective transformed arena. Right, Complex pattern.
</div>
---   

## Submission and Demonstrations
- View our complete project submissions in this [YouTube Playlist](https://youtube.com/playlist?list=PL_9--5xsFYUQ-xg70fmYQrzXn2ip_9O3C&si=z0v1tnEO03IPCXnJ).

---

## Acknowledgments  
**E-Yantra 2023-2024 Robotics Competition**.  
