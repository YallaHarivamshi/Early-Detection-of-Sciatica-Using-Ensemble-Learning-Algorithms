# Early-Detection-of-Sciatica-Using-Ensemble-Learning-AlgorithmsEarly Detection of Sciatica Using Ensemble Learning Algorithms
# Early Detection of Sciatica Using Ensemble Learning Algorithms

## 📌 Project Overview

Sciatica can cause changes in walking patterns, balance, and foot-loading because of irritation or compression of the sciatic nerve. Early gait abnormalities can be difficult to identify through short clinical observations alone.

This project proposes a **wearable, non-invasive system for early screening of sciatica-related gait abnormalities** using motion and plantar-pressure sensors combined with machine learning.

The system continuously collects gait data during natural walking and analyzes the data to classify gait patterns as **Normal** or **Risk**.

> ⚠️ **Note:** This project is intended as an academic early-screening/research system and is not a replacement for professional medical diagnosis.

---

## 🎯 Objectives

- Develop a wearable system to measure lumbar motion and foot-loading during walking.
- Collect motion data using MPU6050 IMU sensors.
- Measure plantar pressure using Force Sensitive Resistors (FSRs).
- Fuse IMU and pressure data to obtain meaningful gait features.
- Apply machine-learning techniques to classify gait abnormalities.
- Provide a compact and non-invasive alternative for gait monitoring.
- Support real-time and offline analysis through mobile synchronization.

---

## 🏗️ System Architecture

The proposed system consists of three major sections:

### 1. Belt Module

The belt module monitors lumbar/trunk motion.

**Main components:**

- ESP32 microcontroller
- Five MPU6050 IMU sensors
- 18650 Li-ion battery
- TP4056 charging module
- MT3608 DC-DC boost converter

The five MPU6050 sensors communicate with the ESP32 through the **I²C interface** and collect acceleration and angular-velocity data.

### 2. Shoe Modules

Two shoe modules are used to monitor foot movement and plantar pressure.

**Each shoe module contains:**

- ESP32 microcontroller
- MPU6050 IMU
- Two FSR sensors
- 10 kΩ resistors
- 18650 Li-ion battery
- TP4056 charging module
- MT3608 boost converter

The FSR sensors generate analog signals related to plantar pressure, while the MPU6050 captures foot-level motion.

### 3. Smartphone Application

The collected sensor information is transferred to a smartphone for processing and analysis.

**Proposed output:**

```text
Normal
   or
Risk
