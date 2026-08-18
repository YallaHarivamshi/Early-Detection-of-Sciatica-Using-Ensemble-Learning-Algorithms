# Early-Detection-of-Sciatica-Using-Ensemble-Learning-AlgorithmsEarly Detection of Sciatica Using Ensemble Learning Algorithms

📌 Project Overview

Sciatica can cause changes in walking patterns, balance, and foot-loading because of irritation or compression of the sciatic nerve. Early gait abnormalities can be difficult to identify through short clinical observations alone.

This project proposes a wearable, non-invasive system for early screening of sciatica-related gait abnormalities using motion and plantar-pressure sensors combined with machine learning.

The system continuously collects gait data during natural walking and analyzes the data to classify gait patterns as Normal or Risk.

«Note: This project is intended as an early-screening/research system and not as a replacement for professional medical diagnosis.»

---

🎯 Objectives

- Develop a wearable system to measure lumbar motion and foot-loading during walking.
- Collect motion data using MPU6050 IMU sensors.
- Measure plantar pressure using Force Sensitive Resistors (FSRs).
- Fuse IMU and pressure data to obtain meaningful gait features.
- Apply machine-learning techniques to classify gait abnormalities.
- Provide a compact and non-invasive alternative for gait monitoring.
- Support real-time and offline analysis through mobile synchronization.

---

🏗️ System Architecture

The proposed system consists of three major sections:

1. Belt Module

The belt module monitors lumbar/trunk motion.

Main components:

- ESP32 microcontroller
- Five MPU6050 IMU sensors
- 18650 Li-ion battery
- TP4056 charging module
- MT3608 DC-DC boost converter

The five MPU6050 sensors communicate with the ESP32 through the I²C interface and collect acceleration and angular-velocity data.

2. Shoe Modules

Two shoe modules are used to monitor foot movement and plantar pressure.

Each shoe module contains:

- ESP32 microcontroller
- MPU6050 IMU
- Two FSR sensors
- 10 kΩ resistors
- 18650 Li-ion battery
- TP4056 charging module
- MT3608 boost converter

The FSR sensors generate analog signals related to plantar pressure, while the MPU6050 captures foot-level motion.

3. Smartphone Application

The collected sensor information is transferred to a smartphone for processing and analysis.

The proposed output is:

Normal
   or
Risk

The block diagram in the project presentation shows the belt and shoe modules being integrated and connected to a smartphone application for sciatica risk detection.

---

🔄 Working Principle

The overall workflow is:

Start
  ↓
Initialize ESP32, MPU6050 and FSR Sensors
  ↓
Collect Sensor Data
  ↓
Filter & Preprocess Signals
  ↓
Extract Gait Features
  ↓
Evaluate Sciatica Risk
  ↓
 ┌───────────────┐
 │               │
Risk           Normal
 │               │
 └───────┬───────┘
         ↓
  Continue Gait Monitoring

The project flow chart follows this sequence: sensor initialization → data acquisition → filtering/preprocessing → gait-feature extraction → risk evaluation → Normal/Risk output.

---

📊 Sensors and Data

The system collects multiple types of biomechanical information.

IMU Data

The MPU6050 sensors provide:

- 3-axis acceleration
- 3-axis angular velocity

These measurements are used to analyze trunk and foot movement.

Plantar Pressure Data

The FSR sensors measure pressure changes under the foot.

The project presentation includes logged multisensor data containing accelerometer, gyroscope, and FSR measurements collected during testing.

---

🤖 Machine Learning

The project focuses on ensemble learning algorithms for identifying gait abnormalities.

The research topic also includes transformer-based feature extraction and ensemble classification models.

The general ML pipeline is:

Raw Sensor Data
       ↓
Signal Preprocessing
       ↓
Sensor Data Fusion
       ↓
Feature Extraction
       ↓
Machine Learning Model
       ↓
Gait Classification
       ↓
Normal / Risk

The proposed system uses gait features such as temporal, symmetry, motion, and pressure-related characteristics.

---

🔬 Research Area

The project belongs to the intersection of:

- Machine Learning
- Wearable Technology
- Gait Analysis
- Biomedical Signal Processing
- Embedded Systems
- Human Motion Monitoring
- Rehabilitation Technology

The research specifically focuses on early detection of sciatica-related gait and biomechanical abnormalities using wearable sensing technologies.

---

🔧 Hardware Components

Component| Purpose
ESP32| Sensor data acquisition and processing
MPU6050| Acceleration and angular-velocity measurement
FSR| Plantar-pressure measurement
18650 Li-ion Battery| Power supply
TP4056| Battery charging
MT3608| DC-DC boost conversion
10 kΩ Resistor| FSR voltage-divider circuit

The belt circuit uses five MPU6050 sensors, while each shoe module uses an MPU6050 and two FSR sensors.

---

💻 Software / Technologies

The project involves:

- Embedded C/C++ for ESP32
- Sensor data acquisition
- Signal preprocessing
- Gait feature extraction
- Machine Learning
- Ensemble Learning
- Transformer-based feature extraction
- Mobile-based data monitoring

---

📈 Project Workflow

Phase 1 — Project Planning

- Idea finalization
- Literature survey
- Component sourcing
- Supply-chain planning

Phase 2 — Hardware Development

- Belt module development
- Shoe module development
- Sensor integration
- Prototype testing

Phase 3 — Software & ML

- Sensor data collection
- Signal preprocessing
- Feature extraction
- Machine-learning implementation
- Mobile application integration

The presentation identifies these phases across the project timeline.

---

🔍 Research Gaps

The project identifies several research gaps:

- Wearable ML-based sciatica detection is still relatively underexplored for real-world monitoring.
- Public wearable gait datasets are limited.
- General-purpose early-screening tools are limited.
- MRI-based diagnosis can be expensive and is not designed for continuous gait monitoring.

These gaps motivate the proposed wearable approach.

---

✅ Expected Outcome

The proposed system aims to:

1. Collect gait and motion data continuously.
2. Detect changes in walking and foot-loading patterns.
3. Extract useful biomechanical features.
4. Classify gait segments as Normal or Risk.
5. Support early screening and monitoring.
6. Provide a compact and non-invasive wearable solution.

The project conclusion describes wearable sensing combined with machine learning as a potential approach for continuous monitoring of gait dynamics and lumbar motion.

---

📁 Suggested GitHub Repository Structure

early-detection-of-sciatica/
│
├── README.md
│
├── hardware/
│   ├── belt-module/
│   ├── shoe-module/
│   └── circuit-diagrams/
│
├── firmware/
│   ├── belt-esp32/
│   └── shoe-esp32/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── machine-learning/
│   ├── preprocessing/
│   ├── feature-extraction/
│   ├── models/
│   └── evaluation/
│
├── mobile-app/
│
├── documentation/
│   ├── project-report/
│   └── presentation/
│
└── LICENSE

---

👥 Project Team

Batch: C11

- Sylada Adithya
- Tamada Kintan Varma
- Yalla Harivamsi
- Vechalapu Saikumar

Project Guide:
Dr. A. Sampath Dakshina Murthy
Associate Professor, Department of ECE

---

🏫 Institution

Vignan's Institute of Information Technology

Department of Electronics and Communication Engineering

---

⚠️ Disclaimer

This project is intended for academic research and early screening support. The Normal/Risk classification should not be considered a medical diagnosis. Clinical assessment by qualified healthcare professionals is required for diagnosis and treatment.

---

📚 References

The project presentation contains references covering sciatica, gait analysis, wearable sensors, machine learning, and biomedical signal processing.

---

⭐ Project Highlights

- Wearable sciatica screening system
- Belt-mounted motion sensing
- Shoe-mounted plantar-pressure sensing
- ESP32-based sensor acquisition
- Multiple MPU6050 IMUs
- FSR-based pressure measurement
- Sensor-data fusion
- Gait feature extraction
- Ensemble learning
- Transformer-based feature extraction
- Normal/Risk classification
- Non-invasive continuous monitoring
