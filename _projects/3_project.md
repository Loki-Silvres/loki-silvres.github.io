---
layout: page  
title: Embedded Toy Detection  
description: Real-time toy detection for mobile robots using advanced object detection models  
img: assets/img/toy_det_image.png
importance: 3  
category: ml_research     
---

This research project enhances a baseline object detection model through advanced techniques such as pseudo-labelling, data engineering, and knowledge distillation. It develops an efficient and scalable **toy detection system** tailored for robotics applications. Leveraging state-of-the-art models like **Co-DETR**, the system pseudo-labels unannotated data to expand the dataset and train a larger model (**DAMO-YOLO-M**) to improve detection accuracy. The deployment model (**DAMO-YOLO-Tiny**) is distilled from the larger variant for lightweight, real-time inference on resource-constrained robotic platforms.

---

## Key Contributions
- **Pseudo-Labelling**: Increased dataset size and diversity by annotating unlabelled data using **Co-DETR**.  
- **Curriculum Learning**: Implemented structured training strategies for **DAMO-YOLO-M**, leading to robust detection performance.  
- **Knowledge Distillation**: Compressed the larger model (**DAMO-YOLO-M**) into a lightweight version (**DAMO-YOLO-Tiny**) for efficient deployment.  
- **Performance Gains**: Achieved a significant improvement in detection accuracy, raising **mAP50** from **34% to 42%**.  
- **Real-Time Deployment**: Deployed on Nvidia DeepStream, integrated seamlessly with **ROS2**, and tested on mobile robots.

---

<div class="row">
   <div class="col-sm mt-6 mt-md-0">
       {% include figure.liquid loading="eager" path="assets/img/toy_inference.png" title="Inference" class="img-fluid rounded z-depth-1" %}
   </div>
   <div class="col-sm mt-6 mt-md-0"> 
       {% include figure.liquid loading="eager" path="assets/img/metric_improv.png" title="Model Improvements" class="img-fluid rounded z-depth-1" %}
   </div>
</div> 
<div class="caption">
   Inference and baseline improvements.
</div>

---

## Workflow and Implementation 

1. **Dataset Augmentation**:  
   Pseudo-labelled unannotated images with **Co-DETR**, creating a larger, high-quality dataset.  

2. **Model Training**:  
   Trained **DAMO-YOLO-M** with curriculum learning to improve robustness. Applied knowledge distillation to develop **DAMO-YOLO-Tiny** for efficient real-time inference.  

3. **Model Deployment**:  
   Integrated the optimized model with **ROS2** and deployed on Nvidia Jetson Nano using **DeepStream SDK** for mobile robotics applications.  

---

## Results

- **Detection Accuracy**:  
  Improved from **34% to 42% mAP50**, ensuring reliable and accurate toy identification.  

- **Deployment Performance**:  
  Achieved **real-time inference** at **15 FPS** on Nvidia Jetson Nano.  

--- 
## Note

The research and experimentation for this project was done in conjunction with my ML intern at Clutterbot Technologies Pvt. Ltd under the mentorship of <a href='https://scholar.google.com/citations?user=kUSzbRAAAAAJ&hl=en'> Mr. Sanchit Tanwar</a>. As such, I am unable to share the source code due to confidentiality reasons.
   