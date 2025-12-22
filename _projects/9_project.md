---
layout: page  
title: MARS - Multimodal Agentic Room Search
description: Agentic RAG for Context-Aware Interior Design
img: assets/img/MARS_demo.png  
importance: 2
category: machine learning
---

### <a href="https://github.com/Loki-Silvres/MARS">[Code]</a> <a href="https://www.kaggle.com/code/alokjayraj/style-search-hybrid-ir-engine">[Demo]</a>

**MARS (Multimodal Agentic Room Search)** is an **Agentic RAG pipeline** designed to solve the "Visual-Semantic Gap" in e-commerce search. Unlike standard vector search engines that rely solely on pixel similarity, MARS employs a fine-tuned Vision-Language Model (VLM) to **reason** about stylistic coherence and functional constraints.

This project demonstrates an end-to-end **GenAI Engineering** workflow: from generating a proprietary synthetic dataset using Teacher-Student distillation to fine-tuning a lightweight agent using QLoRA and optimizing inference latency by **85%**.

---

<div class="row">
   <div class="col-sm mt-3 mt-md-0">
       {% include figure.liquid path="assets/img/MARS_demo.png" title="MARS Pipeline Funnel" class="img-fluid rounded z-depth-1" %}
   </div>
</div>
<div class="caption">
   The 3-Stage MARS Funnel: Classical Filter → Visual Retrieval → Agentic Critique.
</div>

---

## Project details  

### **Features**  
- **Agentic Architecture**: Built a 3-stage funnel combining **BM25**, **SigLIP**, and a **Fine-Tuned VLM**, successfully differentiating between "Visual Matches" (textures/colors) and "Functional Matches" (context).
- **Synthetic Data Engineering**: Created a proprietary dataset of 1,500 visual critiques by deploying **Qwen2.5-VL-7B** as a "Teacher" to label hard-negative pairs mined from the Amazon Berkeley Objects dataset.
- **Resource-Efficient SFT**: Fine-tuned a **Qwen2-VL-2B** model on a single Nvidia P100 GPU using **QLoRA (4-bit quantization)**, achieving SOTA-level reasoning capabilities with minimal compute.
- **Production Optimization**: Implemented **Batched Inference** for the agentic re-ranker, reducing query latency from 3 minutes to **~25 seconds**.

---

## Methodology  

### 1. **The Problem: The Semantic & Visual Gap**  
Standard search fails at complex intent. If a user uploads a photo of a swimming pool and searches for "Bed," Vector Search (CLIP/SigLIP) returns a *blue bed* because it matches the color of the water. It fails to understand that beds do not belong in pools. MARS solves this by introducing a "Reasoning" stage.

### 2. **The 3-Stage Funnel**  
- **Stage 1: The Filter (Classical IR)**:  
  Uses **BM25** to enforce semantic locking. If the user asks for a "Chair," this stage guarantees we retrieve furniture tagged as chairs, filtering out visually similar but wrong categories (e.g., tables).
- **Stage 2: The Vibe Check (Vector Search)**:  
  Uses **SigLIP-so400m** embeddings to re-rank the text candidates based on visual similarity to the user's room image. This filters out items that clash with the room's color palette or texture.
- **Stage 3: The Agent (Reasoning)**:  
  The top candidates are passed to our **Fine-Tuned Qwen2-VL Agent**. The agent looks at the room and the product side-by-side and outputs a compatibility score (0-1) and a natural language rationale (e.g., *"Low Score: This is indoor furniture in an outdoor setting."*).

### 3. **Data Generation Strategy (Teacher-Student)**  
Since no dataset exists for "Interior Design Reasoning," I engineered one:
- **Mining**: Used SigLIP to find "Hard Negatives" (items that look right but are wrong categories).
- **Distillation**: Prompted **Qwen2.5-VL-7B** (The Teacher) to critique these pairs, generating a score and a reasoning trace.
- **Training**: Fine-tuned the smaller **Qwen2-VL-2B** (The Student) to mimic this reasoning logic.

---

## Insights & Conclusion  

- **Vectors imply Vibe, Agents imply Logic**: Embedding models are excellent for surface-level matching (color/texture) but lack world knowledge. Integrating a small VLM agent adds the necessary "Common Sense" layer to search.
- **Synthetic Data is King**: A small 2B parameter model, when fine-tuned on high-quality, task-specific synthetic data, can outperform larger generalized models in specific reasoning tasks.
- **Hybrid Retrieval is Mandatory**: Relying purely on Vector Search often leads to semantic drift. Anchoring the search with Classical Retrieval (BM25) provided the necessary stability for the agent to work effectively.

---

### **Links**
- **Github**: [https://github.com/Loki-Silvres/MARS](https://github.com/Loki-Silvres/MARS)
- **Demo Notebook**: [Kaggle - Hybrid IR Engine](https://www.kaggle.com/code/alokjayraj/style-search-hybrid-ir-engine)
- **Amazon Berkeley Objects (ABO)**: [ABO Dataset link](https://www.kaggle.com/datasets/umeshrawat7/amazon-berkeley-objects)
- **House Rooms Dataset**: [Rooms Dataset link](https://www.kaggle.com/datasets/annielu21/house-rooms)
- **Synthetic Dataset**: [My Dataset link](https://www.kaggle.com/datasets/alokjayraj/style-search-qwen2-5vl-generated-pairs)