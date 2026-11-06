# Night-Time Object Detection Using YOLO11n and Image Enhancement

## Project Overview

Night-Time Object Detection is an experimental Computer Vision project focused on improving object detection under low-light conditions.

Object detection becomes challenging at night due to poor illumination, reduced contrast, shadows, and visibility issues. These conditions can affect model performance, resulting in missed detections and false positives.

This project explores the use of a lightweight YOLO11n object detection model combined with image enhancement techniques to investigate detection performance in nighttime environments.

The primary objective is to study how preprocessing techniques, particularly Contrast Limited Adaptive Histogram Equalization (CLAHE), influence object detection results under challenging lighting conditions.

## Research Motivation

Most object detection models perform better when objects are clearly visible. However, nighttime environments introduce several challenges:

- Low illumination and poor visibility.
- Reduced contrast between objects and backgrounds.
- Difficulty detecting pedestrians and small objects.
- False positive detections caused by background noise and lighting effects.

This project investigates whether image enhancement can help improve object visibility and support more reliable object detection in low-light environments.

## Objectives

- Explore object detection performance in nighttime images.
- Implement a lightweight YOLO11n model.
- Apply CLAHE for local contrast enhancement.
- Experiment with different confidence and IoU thresholds.
- Compare detection outputs before and after image enhancement.
- Analyse false positives and missed detections.
- Investigate possible improvements for challenging nighttime conditions.

## Technologies and Tools

| Technology | Purpose |
|---|---|
| Python | Implementation |
| YOLO11n | Object detection |
| OpenCV | Image processing and enhancement |
| CLAHE | Low-light image enhancement |
| Google Colab | Experimental environment |
| NumPy | Numerical operations |
| Matplotlib | Result visualization |

## Methodology

The current experimental workflow consists of the following stages:

### 1. Input Image

Nighttime images are used as input to investigate object detection under low-light conditions.

### 2. Baseline Object Detection

A pretrained YOLO11n model is used to detect objects in the original nighttime images.

The model produces:
- Object class labels.
- Bounding boxes.
- Detection confidence scores.

### 3. Image Enhancement Using CLAHE

CLAHE (Contrast Limited Adaptive Histogram Equalization) is applied to improve local contrast and reveal details in darker image regions.

Unlike global histogram equalization, CLAHE enhances contrast locally while limiting excessive amplification.

Different CLAHE settings are experimented with to observe their impact on detection results.

### 4. Detection After Enhancement

The enhanced images are passed through YOLO11n to examine whether improved visual contrast leads to better object detection.

### 5. Experimental Comparison

The original and enhanced image detection results are compared to investigate:

- Changes in detection confidence.
- Missed pedestrian detections.
- False positive detections.
- Effects of different preprocessing parameters.

## Experiments Performed

### 1. Confidence Threshold Experiments

Different confidence thresholds were tested to understand their effect on detection outputs.

A lower confidence threshold can retain weaker detections but may also introduce more false positives.

### 2. IoU Threshold Experiments

IoU (Intersection over Union) thresholds of 0.30 and 0.45 were explored to investigate bounding-box overlap and duplicate detection behaviour during non-maximum suppression.

### 3. CLAHE Experiments

Different CLAHE clip limit values, including 1.5 and 2.0, were tested.

The experiments showed that image enhancement can improve the visibility of some objects, but excessive enhancement may also amplify background details and introduce unwanted detections.

## Initial Observations

The initial experiments provided the following observations:

- CLAHE improved the visibility of certain objects in nighttime images.
- A CLAHE clip limit of 1.5 showed promising detection confidence improvements in some tested cases.
- Increasing the enhancement strength did not consistently improve detection.
- Some background regions produced false positive detections.
- Pedestrians remained challenging to detect under certain lighting conditions.
- Confidence and IoU threshold adjustments influenced the detection outputs.

These are preliminary observations from experimental testing, not final benchmark results.

## Current Project Status

**Status: Initial Experimental Prototype**

The project currently focuses on implementing YOLO11n, experimenting with image enhancement, and analysing detection outputs.

It is not yet a fully validated research solution. Further experiments and quantitative evaluation are required to establish whether the proposed approach consistently improves nighttime object detection.

## Future Work

The following improvements are planned:

1. Experiment with additional image enhancement techniques.
2. Evaluate performance on a larger and more diverse nighttime dataset.
3. Compare original and enhanced images using quantitative metrics.
4. Investigate lightweight object detection models for resource-constrained environments.
5. Evaluate Precision, Recall, F1-score, mAP, and inference time.
6. Investigate approaches for reducing false positives and missed pedestrian detections.
7. Explore a more robust nighttime object detection pipeline.

## Research Direction

The broader research direction is to investigate efficient and reliable object detection under challenging nighttime conditions.

The project aims to explore the relationship between image enhancement and object detection performance, with potential applications in intelligent transportation, surveillance, and autonomous systems.

## Author

**Maheen Zaheer**

Computer Engineering Student  
University of Engineering and Technology (UET), Lahore

GitHub: [MaheenZaheer](https://github.com/MaheenZaheer)

---

*This repository documents an ongoing experimental project and its preliminary findings. Research contributions and performance improvements will be updated as further experiments are conducted.*
