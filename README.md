# Smart-Fruit-Ripeness-Detection-System
It is an automated solution designed to accurately assess fruit ripeness and quality while overcoming the limitations of traditional manual inspection methods, which are subjective and time-consuming. The system uses a camera module mounted on a rotator to capture fruit images from multiple angles, ensuring complete surface coverage. These images are processed using edge detection and deep learning techniques, where a Convolutional Neural Network (CNN) analyzes visual features such as color, texture, and defects to classify fruits as healthy, ripe, or rotten.

Along with image-based analysis, the system monitors environmental and biochemical factors that affect fruit freshness. A DHT11 sensor measures temperature and humidity in real time, while an MQ-3 gas sensor detects ethanol vapors released during fruit ripening and spoilage. An Arduino Uno integrates sensor data with CNN predictions, and the final results are transmitted to the cloud and displayed on a mobile or web application, enabling real-time monitoring and informed decision-making.
# Project Overview
Fruits are highly perishable, and inaccurate ripeness assessment leads to significant post-harvest losses across the agricultural supply chain. Conventional inspection methods rely on human judgment based on color, smell, or texture, making them subjective, inconsistent, and unsuitable for large-scale operations.

This project presents a Smart Fruit Ripeness Detection and Quality Monitoring System that integrates:

-Multi-angle image acquisition using a motorized rotator

-CNN-based visual classification

-Environmental sensing (temperature & humidity)

-Biochemical sensing (ethanol gas detection)

-By fusing computer vision, deep learning, and IoT, the system provides a robust, scalable, and industry-ready solution for fruit quality monitoring.
# Key Features

-Multi-Angle Fruit Image Capture (360° Rotation)

-CNN-Based Ripeness Classification

-Edge Detection for Enhanced Feature Extraction

-Real-Time Temperature & Humidity Monitoring (DHT11)

-Ethanol Gas Detection for Spoilage Identification (MQ-3)

-Hybrid Decision Logic (Sensor + CNN Fusion)

-Cloud-Based Data Transmission

-Mobile/Web Dashboard for Live Monitoring

-Non-Destructive and Automated Inspection
# Hardware Components Used
| S.No | Component                     | Description                    |
| ---- | ----------------------------- | ------------------------------ |
| 1    | Arduino Uno                   | Central control unit           |
| 2    | Camera Module / Laptop Camera | Image acquisition              |
| 3    | DHT11 Sensor                  | Temperature & humidity sensing |
| 4    | MQ-3 Gas Sensor               | Ethanol vapor detection        |
| 5    | 28BYJ-48 Stepper Motor        | Fruit rotation                 |
| 6    | ULN2003 Driver Module         | Stepper motor control          |
| 7    | Breadboard & Jumper Wires     | Circuit connections            |
| 8    | Power Supply                  | System operation               |
# Software & Technologies
-Python

-OpenCV (Image Processing & Edge Detection)

-TensorFlow / Keras (CNN Model)

-Arduino IDE

-Embedded C

-IoT Cloud Platform

-Mobile / Web Dashboard
# System Workflow
1)Fruit Placement

Fruit is placed on a motorized rotating platform.

2)Automated Rotation

Stepper motor rotates the fruit in 10° increments

A total of 36 images are captured for full surface coverage

3)Image Acquisition

Camera captures images after each rotation

Ensures reduced shadowing and occlusion

4)Image Preprocessing

Resize to 224 × 224

Normalization

Edge detection to enhance surface defects

5)CNN-Based Classification

Model analyzes color, texture, and surface patterns

Predicts: Healthy / Ripe / Rotten

6)Sensor-Based Monitoring

DHT11 measures temperature and humidity

MQ-3 detects ethanol vapor concentration

7)Hybrid Decision Logic

If ethanol > threshold → Fruit classified as Rotten

Else → CNN prediction is accepted

8)Cloud & Dashboard Update

Final results sent to cloud

Displayed on mobile/web application
# Results & Observations
✔️ Unripe fruits showed low ethanol levels (<5%)

✔️ Ripe fruits exhibited moderate ethanol release

✔️ Rotten fruits exceeded 15% ethanol concentration

✔️ Multi-angle imaging significantly improved classification accuracy

✔️ Sensor + CNN fusion corrected false positives

✔️ System performed reliably under real-time testing
# Future Scope and Enhancements
The system can be extended by incorporating higher-sensitivity gas sensors and larger, more diverse training datasets to improve accuracy across different fruit varieties. Deployment on edge devices such as ESP32 or Jetson Nano can enable real-time inference without dependency on external systems. Integration with supply chain platforms, automated sorting mechanisms, and predictive shelf-life analytics can transform the solution into a scalable, industry-grade smart agriculture product.
