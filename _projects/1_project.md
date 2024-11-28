---
layout: page
title: Autonomous Driving B3RB-buggy
description: Advanced Autonomous Driving System for NXP-AIM'24
img: assets/img/b3rb_buggy.jpg
importance: 1
category: robotics
related_publications: true
---
### <a href="https://github.com/Loki-Silvres/Autonomous-Driving-B3RB-buggy">[Code]</a>

The B3RB Autonomous Driving project represents a comprehensive exploration of robotic perception and autonomous navigation, developed as part of the NXP-AIM'24 challenge. Our team successfully created an intelligent robotic platform that demonstrates advanced capabilities in real-time environmental interpretation and autonomous decision-making.

<div class="row">
   <div class="col-sm mt-6 mt-md-0">
       {% include figure.liquid loading="eager" path="assets/img/lidar_camera_testing.png" title="LIDAR and Camera Detection" class="img-fluid rounded z-depth-1" %}
   </div>
   <div class="col-sm mt-6 mt-md-0"> 
       {% include figure.liquid loading="eager" path="assets/img/model_testing.png" title="Model Inference" class="img-fluid rounded z-depth-1" %}
   </div>
</div>
<div class="caption">
   Project highlights: LIDAR-based perception and dynamic Object Detection. 
</div>

## Technical Architecture

The autonomous system was built on a robust technological stack, integrating multiple advanced perception and control mechanisms:

- **Computational Platform**: Mini computer running ROS2 on Ubuntu 22
- **Perception Systems**:
   . - LIDAR for environmental mapping
   . - Camera for lane detection and traffic sign recognition
- **Control Mechanism**: Ackermann-steering control for precise navigation
- **Machine Learning Model**: YOLOv5s with INT8 quantization

## Key Achievements

- **Performance Milestone**: Achieved an impressive 1:42 track time
- **Real-time Inference**: Maintained 7 Hz processing speed
- **Advanced Perception**: Implemented comprehensive obstacle detection and lane tracking
- **Optimization**: Utilized NPU-optimized model for efficient processing

<iframe width="930" height="450" src="https://www.youtube.com/embed/n6aP2X9CODE" title="Simulation Demonstration" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
       {% include figure.liquid path="assets/img/b3rb_simulation.png" title="Simulation Performance" class="img-fluid rounded z-depth-1" %}
   </div> 
   <div class="col-sm-4 mt-3 mt-md-0">
       {% include figure.liquid path="assets/img/buggy_on_track.jpeg" title="Buggy on Track" class="img-fluid rounded z-depth-1" %}
   </div>
   <div class="col-sm-4 mt-3 mt-md-0">
       {% include figure.liquid path="assets/img/buggy_block-diagram.png" title="Block Diagram" class="img-fluid rounded z-depth-1" %}
   </div>
</div>
<div class="caption"> 
   Detailed views of track performance metrics and system architecture.
</div>
---
 
## Note
The grand finale videos are unavailable due to NXP-Semiconductors office regulations.

---    