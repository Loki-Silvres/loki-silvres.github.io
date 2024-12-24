---
layout: page
title: Mobile-Swarm-Navigation
description: Multi-Robot Autonoumous Semantic Exploration and Navigation
img: assets/video/3_final.gif
importance: 1
category: robotics
---
### <a href="https://github.com/Loki-Silvres/Mobile-Swarm-Navigation">[Code]</a>

The Autonomous Swarm Navigation System leverages advanced AI and robotics frameworks to enable coordinated multi-robot mapping, task allocation, and semantic exploration of dynamic environments. This project was developed to showcase innovative swarm robotics solutions for real-world applications.

<div class="row">
   <div class="col-sm mt-6 mt-md-0">
       {% include figure.liquid loading="eager" path="assets/video/Multi_explore_merge.gif" title="Autonomous Mapping" class="img-fluid rounded z-depth-1" %}
   </div> 
   <div class="col-sm mt-6 mt-md-0"> 
       {% include figure.liquid loading="eager" path="assets/img/Object_map.png" title="Stereo Depth Sensing" class="img-fluid rounded z-depth-1" %}
   </div>
</div>
<div class="caption">
   Robots performing mapping and depth sensing for semantic understanding of the environment.
</div>


## System Overview

The system employs a Central Nervous System (powered by a Large Language Model) to:
- Process textual commands.
- Coordinate robot tasks through a scheduler.
- Manage dynamic state updates for swarm efficiency.

<div class="row">
   <div class="col-sm mt-6 mt-md-0">
       {% include figure.liquid loading="eager" path="assets/video/Environments.gif" title="Swarm Navigation" class="img-fluid rounded z-depth-1" %}
   </div>
   <div class="col-sm mt-6 mt-md-0">
       {% include figure.liquid loading="eager" path="assets/img/Waffle.png" title="Robot" class="img-fluid rounded z-depth-1" %}
   </div>  
</div>
<div class="caption"> 
   Left: Environments used. Right: Robot used.
</div>

Unit robots autonomously execute tasks such as:

- **SLAM**: Simultaneous Localization and Mapping.
- **Stereo Depth Sensing**: For spatial perception.
- **Instance Segmentation**: To generate a object map of the environment and add them to a shared dynamic database.

These capabilities enable seamless task navigation, manipulation, and exploration within dynamic environments.

<div class="row">
   <div class="col-sm mt-6 mt-md-0">
       {% include figure.liquid loading="eager" path="assets/video/Swarm_Navigation.gif" title="Swarm Navigation" class="img-fluid rounded z-depth-1" %}
   </div>
</div>
<div class="caption">
   Dynamic goal assignment and planning in a swarm of robots.
</div>

### Highlights:
- Real-time map generation and semantic updates.

<div class="row">
   <div class="col-sm mt-6 mt-md-0">
       {% include figure.liquid loading="eager" path="assets/video/Dynamic_database.gif" title="Swarm Navigation" class="img-fluid rounded z-depth-1" %}
   </div>
</div>
<div class="caption">
   Dynamic Semantic Mapping.
</div>

- Coordinated task allocation with minimal redundancy.
- Efficient coverage of unknown environments through collaborative exploration.

## Future Work

- **Integration with Robotic Arms**: Increase of Task Space with added manipulation tasks.
- **Simultaneous Exploration and Navigation**: Merging of the 2 phases of Exploration and Navigation.

---

