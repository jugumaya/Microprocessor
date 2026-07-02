# IoT & AI-Driven Maternal Healthcare Monitoring System

A wearable biomedical prototype designed for real-time health tracking of pregnant mothers and fetuses. This project bridges hardware engineering with intelligent data analysis to provide continuous, non-invasive prenatal care—making vital monitoring accessible anytime, anywhere.

---

## Project in a Nutshell
Traditional monitoring equipment (like clinical CTG machines) is usually bulky, expensive, and restricted to hospitals. This prototype serves as an affordable, portable solution to bridge that gap, ensuring continuous safety and peace of mind during pregnancy, especially in remote or low-resource areas.

---

## How It Works
The system connects hardware engineering with cloud analytics through three distinct layers:

### 1. Smart Sensing (Hardware Layer)
A wearable device equipped with biomedical sensors continuously collects vital data from both the mother and the fetus:
* **ADXL345 Accelerometer:** Tracks movement and triggers alerts for sudden falls or physical distress.
* **MAX30102 Pulse Oximeter:** Measures Heart Rate (BPM) and Blood Oxygen Saturation ($SpO_2$).
* **DS18B20 Temperature Sensor:** Records real-time body temperature fluctuations.

### 2. The Brains (Microprocessor & IoT Layer)
* **ESP32-C3 Microcontroller:** Acts as the central processing core engine, ingesting raw sensor readings, filtering noise, and using its built-in Wi-Fi module to transmit data wirelessly.
* **Blynk IoT Cloud Platform:** Receives data streams securely in real time with an average network latency of just **300 ms**, enabling remote data visualization via a desktop and mobile dashboard.

### 3. Intelligent Analysis (AI Concepts & Automation)
The system consistently monitors incoming logs against predefined safe clinical thresholds. If any critical metric (e.g., severe fever, abnormal heart rhythm, drops in $SpO_2$, or sudden acceleration indicating a fall) is detected, it instantly triggers an automated emergency alarm notifying both the mother and her healthcare provider.

---

##  Why It Matters (The Impact)
* **From Reactive to Proactive:** Instead of waiting for the next clinic visit, doctors and mothers can catch potential complications early, preventing critical emergencies.
* **Bridging the Healthcare Gap:** By lowering costs and removing the need for stationary clinical equipment, it brings high-quality prenatal monitoring to underserved or remote communities.
* **Empowering Mothers:** Provides real-time, transparent insights into the pregnancy journey, reducing maternal anxiety and enhancing remote telemedicine communication with obstetricians.

---

## 👥 Contributions & Documentation
This project represents a collaborative intersection of hardware development, IoT architecture, and biomedical research.


### 📄 Reference Paper
The foundational research methodology, detailed system block diagrams, mathematical calibration algorithms, and laboratory testing findings are fully documented in the accompanying research paper included in this repository: IoT_and_AI_in_Maternal_Healthcare_Monitoring.pdf
