# wearable-iot-health-tracker
Compact wearable IoT health and activity tracker using ESP32, MAX30102 biometric sensor, and cloud MQTT telemetry.
# ⌚ Wearable IoT Health & Activity Tracker

> A low-power, wrist-mounted biometric telemetry node designed to monitor real-time heart rate, blood oxygen levels (SpO2), and step count, transmitting live health metrics to a cloud dashboard via Wi-Fi.

[![Status](https://img.shields.io/badge/Status-Completed-emerald?style=for-the-badge)]()
[![MCU](https://img.shields.io/badge/MCU-ESP32_/_ESP8266-blue?style=for-the-badge)]()

---

## 🎯 Overview & Mission Objective
Continuous health monitoring at the edge allows for early detection of physiological anomalies. This wearable device integrates optical pulse oximetry and motion tracking sensors into a compact form factor, enabling personal health tracking and remote caregiver alerting.

---

## 🛠️ Bill of Materials (BOM)
| Component | Specification / Role |
| :--- | :--- |
| **ESP32-PICO / ESP8266 (Mini)** | Ultra-compact Wi-Fi microcontroller for data processing and transmission |
| **MAX30102 Sensor Module** | Integrated pulse oximetry and heart-rate optical sensor |
| **MPU6050 6-Axis Accelerometer** | Step counting and physical activity/fall detection |
| **0.96" OLED Display (SSD1306)** | Real-time local visualization of health metrics |
| **Power Architecture** | Rechargeable LiPo battery with TP4056 charging circuit |

---

## 📌 GPIO Pinout Mapping (I2C Bus)
| Component | Component Pin | Microcontroller Pin | Engineering Function |
| :--- | :--- | :--- | :--- |
| **MAX30102 Biometric Sensor** | `SDA / SCL` | `GPIO 21 / 22 (I2C)` | Heart Rate & SpO2 Data Bus |
| **MPU6050 Accelerometer** | `SDA / SCL` | `GPIO 21 / 22 (I2C)` | Motion & Step Counting Bus |
| **SSD1306 OLED Display** | `SDA / SCL` | `GPIO 21 / 22 (I2C)` | Visual Telemetry Interface |

---

## 📂 Repository Structure
```text
📂 wearable-iot-health-tracker
├── 📂 firmware             <-- C++ source code (wearable_health_node.ino)
├── 📂 schematics           <-- I2C shared bus and battery power layout
└── 📄 README.md            <-- Project documentation
