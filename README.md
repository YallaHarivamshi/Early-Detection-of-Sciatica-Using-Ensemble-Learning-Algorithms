# Early Detection of Sciatica using Ensemble Learning Algorithms

## 📌 Project Overview

This project focuses on the early detection of sciatica-related gait abnormalities using wearable sensors and machine learning techniques.

The proposed system uses a belt-mounted IMU and shoe-mounted plantar-pressure sensors to collect gait data during natural walking. The collected sensor data is processed to extract gait-related features and classify normal and abnormal gait patterns.

The system aims to provide a compact, non-invasive approach for continuous monitoring and early screening of sciatica-related gait abnormalities.

## 🎯 Objectives

* Develop a wearable system to measure lumbar motion and foot-loading during natural walking.
* Collect gait data using IMU and plantar-pressure sensors.
* Fuse motion and pressure data to extract gait features.
* Use lightweight machine-learning models to classify gait segments as Normal or Risk.
* Enable early identification of sciatica-related gait abnormalities.
* Support continuous and non-invasive gait monitoring.

## 🔬 Research Area

* Early detection of sciatica-related gait and biomechanical abnormalities.
* Wearable sensing technologies.
* Machine learning for gait classification.
* Continuous health monitoring.
* Rehabilitation and mobility monitoring.

## 🛠️ System Components

### Belt Module

The belt module uses:

* ESP32 microcontroller
* MPU6050 IMU sensors
* 3.7 V 18650 Li-ion battery
* TP4056 charging controller
* MT3608 DC-DC boost converter

The belt-mounted IMUs capture motion information around the waist region.

### Shoe Module

The shoe module uses:

* ESP32 microcontroller
* MPU6050 IMU
* Force Sensitive Resistors (FSRs)
* 10 kΩ voltage-divider networks
* 3.7 V 18650 Li-ion battery
* TP4056 charging controller
* MT3608 DC-DC boost converter

The shoe module captures foot-level motion and plantar-pressure information.

## ⚙️ Working Principle

1. Motion data is collected from the belt-mounted IMU sensors.
2. Plantar-pressure data is collected from the shoe-mounted pressure sensors.
3. Sensor signals are synchronized and filtered.
4. Motion and pressure data are combined to represent gait dynamics.
5. Relevant gait features are extracted.
6. Machine-learning models classify gait patterns.
7. The system generates a sciatica risk indication for early screening.

## 📊 Machine Learning

The project focuses on machine-learning-based classification of gait abnormalities.

The presentation describes the use of ensemble learning and transformer-based feature extraction for analyzing sensor data and classifying normal and abnormal gait patterns.

## 🔄 Project Workflow

```text
Wearable Sensors
       ↓
Sensor Data Collection
       ↓
Signal Synchronization & Filtering
       ↓
Data Fusion
       ↓
Feature Extraction
       ↓
Machine Learning
       ↓
Gait Classification
       ↓
Risk Identification
```

## 📋 Project Scope

The project aims to design and implement a wearable multi-sensor system combining lumbar IMU and plantar-pressure sensing for gait analysis.

The system is intended to extract temporal, symmetry, and pressure-based gait features and classify short gait segments as Normal or Risk.

It also considers real-time and offline analysis through mobile synchronization and optional cloud processing.

## 🔍 Research Gaps

The project identifies the following research gaps:

* MRI-based diagnosis can be costly and may identify sciatica after significant nerve irritation.
* Wearable ML-based sciatica detection is still underexplored for real-world monitoring.
* Limited public wearable gait datasets can affect model generalization.
* Accessible early-screening tools for the general population are limited.

## 📈 Expected Outcome

The proposed system is intended to provide a non-invasive approach for monitoring gait dynamics and lumbar motion.

Combining wearable sensor data with machine-learning models can help identify subtle gait changes associated with sciatica-related abnormalities and support early screening.

## 👥 Project Team

| Name                | 
| ------------------- |
| Sylada Adithya      | 
| Tamada Kintan Varma | 
| Yalla Harivamsi     | 
| Vechalapu Saikumar  |         |

### Project Guide

**Dr. A. Sampath Dakshina Murthy**
Associate Professor
Department of ECE

## 📂 Project Files

* [Project Presentation](./Early_Detection_of_Sciatica_Project_Presentation.pptx)

## 🏫 Project Information

**Area:** Machine Learning
**Batch:** C11
**Department:** Electronics and Communication Engineering

## 📚 References

The project presentation includes references covering sciatica, gait analysis, wearable sensors, plantar-pressure analysis, and machine-learning approaches for biomedical signal processing.

## ⚠️ Disclaimer

This project is intended for academic and research purposes. The proposed system is designed for early screening and monitoring and should not be considered a replacement for professional medical diagnosis.
