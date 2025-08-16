# Smart Sorting Robot for Food Packaging

A vision-based robotic system designed to detect packaging defects in food products and sort them automatically on a conveyor belt. This project combines computer vision, deep learning, and robotic control to streamline quality assurance in food warehouses.

---

## Project Overview

The robot monitors a conveyor belt carrying packaged food items. Using a high-resolution camera and a trained classification model, it identifies defective packaging. If a defect is detected, the robotic arm picks up the item and places it in a bin behind the robot. Otherwise, the item continues down the conveyor.

---

## Features

- Real-time image capture and defect detection
- Deep learning classification model (CNN-based)
- Robotic arm with 5 degrees of freedom
- Automated sorting into defect bin
- Modular design for easy integration into warehouse systems

---

## Demo

[Sorting Robot design sketch](https://creativeschoolarabia.com/wp-content/uploads/2021/03/moon-50k.jpg)

---

## Execution Algorithm

```bash
1. Receive packaged product on the conveyor belt
2. Capture an image using a high-resolution camera
3. Analyze the image using a trained classification model (e.g., CNN)
4. If the product is defect-free:
    - Let it continue on the conveyor
5. If the product has a packaging defect:
    - Activate the robotic arm
    - Pick up the product from the conveyor
    - Rotate or extend the arm backward
    - Drop the product into the defect bin behind the robot
6. Return to standby mode for the next product
```

---

## Enviromintal + Robotic Design

| Component | Describtion |
|----------|----------|
| Camera    | Industrial-grade camera (e.g., 1080p) mounted above the conveyor   |
| Clasification Model   | Deep learning model trained on images of good vs. defective packaging (e.g., TensorFlow or PyTorch)   |
| Robotic Arm | 5-DOF arm capable of picking and placing items |
| Defect Bin | Container placed behind the robot to collect defective products |
| Control Unit | Jetson Nano or Raspberry Pi with GPU support for real-time inference |
| Mobility | Stationary setup; only the arm moves |

---

## Working Envelope Elements

- Field of Vision = Full conveyor width
- Processing time = Less than 1 second per product for detection and decision
- Arm Reach = From conveyor to defect bin
- Payload Capacity = Up to 2 kg per product
- Detection Accuracy = Minimum 95% classification accuracy
