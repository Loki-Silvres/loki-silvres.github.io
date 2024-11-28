---
layout: page  
title: Warehouse Drone  
description: Navigation and Control Systems  
img: assets/img/wd_sim_drone.png  
importance: 10  
category: robotics  
---

### <a href="https://github.com/Loki-Silvres/Warehouse-Drone">[Code]</a>

This project focuses on developing an autonomous **Warehouse Drone** for the **e-Yantra 2023-24 competition**, leveraging advanced techniques in navigation, control systems, and simulation. The drone is designed to autonomously navigate a confined warehouse environment, localize itself, and perform tasks efficiently.

---
<iframe width="930" height="450" src="https://www.youtube.com/embed/tMtO-cpKz9Y" title="Warehouse Drone Demonstrations" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

---

### Key Features:
- **Navigation**: Implemented A* algorithm for optimal pathfinding in cluttered environments.  
- **Control Systems**: Used **PID tuning** for precise control over drone movements, ensuring smooth and accurate navigation.  
- **Localization**: Applied computer vision techniques to accurately determine the drone’s position within the environment.  
- **Simulation**: Developed and tested in **Gazebo Ignition**, providing a realistic simulation environment to fine-tune performance.  

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/wd_simulation_2.png" title="Simulation Environment" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0"> 
        {% include figure.liquid loading="eager" path="assets/img/path.png" title="Pathfinding in Action" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Simulation environment in Gazebo Ignition. Right: A* pathfinding visualization during navigation.
</div>

---

## Progress and Results

- Successfully cleared **Stage 1** of the competition.  
- Currently ranked **15th** in the ongoing leaderboard.  
- Demonstrated robust control and navigation capabilities under simulation conditions.  

---

## Workflow and Methodology

1. **Navigation Algorithm**:  
   - Implemented **A*** for computing the shortest path between start and goal locations, optimizing for obstacles in the environment.

2. **Control Systems**:  
   - Tuned **PID controllers** for maintaining stable and responsive drone movement.

3. **Localization**:  
   - Leveraged computer vision techniques such as feature matching for precise localization.

4. **Simulation and Testing**:  
   - Utilized **Gazebo Ignition** for a realistic warehouse simulation environment to iterate and refine drone behavior.

---

## Future Goals

- Advance to the next competition stage by further improving navigation efficiency and robustness.  
- Transition from simulation to hardware deployment for real-world testing.

