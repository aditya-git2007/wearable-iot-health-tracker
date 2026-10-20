# Wearable IoT Health Tracker — Wiring & Power Guidelines

## ⚡ Shared I2C Bus & Power Architecture
* **Multi-Sensor I2C Bus:** The MAX30102 optical sensor, MPU6050 accelerometer, and SSD1306 OLED display all share the same I2C bus (`SDA` and `SCL`), relying on unique device addresses to prevent data collisions.
* **Wearable Power Management:** Powered by a compact 3.7V LiPo battery routed through a TP4056 charging module and a 3.3V low-dropout (LDO) regulator to ensure stable voltage for sensitive optical biosensors.
