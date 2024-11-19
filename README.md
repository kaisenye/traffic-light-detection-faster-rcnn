# Traffic Light Detection for Autonomous Vehicles

## Overview

This project focuses on the development and comparison of advanced object detection systems, primarily **Faster R-CNN** and **YOLOv3**, to enhance traffic light detection for autonomous and semi-autonomous vehicles. By leveraging **Convolutional Neural Networks (CNNs)**, the models aim to accurately detect and classify traffic lights under diverse urban driving conditions, playing a crucial role in enabling safe and efficient navigation for autonomous vehicles.

### Key Features
- **Model Type:** Traffic Light Detection
- **Architecture:** 
  - Faster R-CNN with MobileNetV2 Backbone
  - YOLOv3 with ResNet-50 Backbone
- **Detection Classes:** `go`, `warning`, `stop`, `goLeft`, `warningLeft`, `stopLeft`, and `background`
- **Input:** Images with 1280x960 resolution
- **Output:** Traffic light bounding box coordinates and labels
- **Dataset:** [LISA Traffic Light Dataset](https://www.kaggle.com/datasets/mbornoe/lisa-traffic-light-dataset/)

---

## Getting Started

### Prerequisites
- **Python Version:** 3.8 or above
- **Dependencies:**
  - `torch`
  - `torchvision`
  - `pandas`
  - `numpy`
  - `matplotlib`
- **Hardware:**
  - GPU with sufficient memory for training (e.g., NVIDIA Tesla K80 or better)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/usc-viterbi/traffic-light-detection.git
   cd traffic-light-detection
2. Install the required Python libraries:
   ```bash
   pip install -r requirements.txt

---

## Results
### Faster R-CNN
- Backbone: MobileNetV2
- Metrics:
  - Intersection over Union (IoU) threshold: 0.5
  - Precision: Moderate
  - Recall: Moderate
- Strengths: Strong feature extraction, robust to varied lighting conditions
- Limitations: Moderate precision and recall require further optimization
### YOLOv3
- Backbone: ResNet-50
- Metrics: Unable to complete training due to batch sizing issues
- Strengths: Real-time processing potential
- Limitations: Computational challenges on limited GPUs

---

## Challenges and Learnings

### Challenges
1. **Batch Sizing Issues:** Persistent problems with YOLOv3 due to dataset format and GPU constraints.
2. **Preprocessing Errors:** Initial resizing of images caused mismatches with bounding box annotations.
3. **Limited Resources:** GPU constraints limited exploration of advanced architectures like YOLOv4.

### Learnings
1. Proper alignment between preprocessing and annotations is crucial.
2. Faster R-CNN’s performance can be significantly impacted by the choice of backbone.
3. YOLOv3 requires careful tuning and resource management for successful training.

---

## Acknowledgements

- **LISA Traffic Light Dataset:** [LISA Traffic Light Dataset](https://www.kaggle.com/datasets/mbornoe/lisa-traffic-light-dataset/)
- Inspired by research from:
  - Ren et al., *“Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks”*
  - He et al., *“Mask R-CNN”*


