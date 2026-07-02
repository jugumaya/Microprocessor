# IoT and AI-Based Maternal Healthcare Monitoring System

An IoT-powered wearable healthcare system designed for real-time remote prenatal care, aiming to reduce maternal mortality rates, especially in resource-constrained environments. This project was developed as part of an academic research course at Independent University, Bangladesh (IUB).

---

##  Authors
* **Samiul Haque**
* **Raisa Tafannum** 
* **MD Rayhan Hossain** 
* **Jugumaya Saha Disha**

*Department of Computer Science and Engineering (CSE), Independent University, Bangladesh (IUB).*

## 📌 Project Overview
This system integrates biomedical sensors with an **ESP32-C3** microcontroller to track critical physiological parameters of expectant mothers. The collected data is transmitted wirelessly to the **Blynk IoT Cloud Platform** for real-time monitoring and anomaly detection. If any vital sign crosses a predefined safe threshold, the system triggers an emergency alert instantly.

### Key Features:
* **Continuous Monitoring:** Tracks vital signs automatically every 3 minutes.
* **Cloud Integration:** Real-time data visualization on both Mobile and Desktop via Blynk IoT App.
* **Fall & Motion Detection:** Built-in alert mechanism for sudden falls or physical distress.
* **Automated Alerts:** Instant emergency notification system if health metrics exceed thresholds.
* **Low Latency:** Average data transmission latency of just **300 ms** from sensor to cloud.

---

## 🛠️ System Architecture & Hardware Components

The system architecture follows a seamless pipeline: **Sensors (Perception) ➡️ ESP32-C3 (Gateway) ➡️ Blynk Cloud (Storage & Processing) ➡️ Mobile/Desktop App (User Interface).**

### Hardware Specification:
| Component | Model/Type | Key Functionality |
| :--- | :--- | :--- |
| **Microcontroller** | ESP32-C3 | Core processing unit with built-in Wi-Fi & I2C/One-Wire protocols. |
| **Pulse Oximeter** | MAX30102 | Measures Heart Rate (BPM) and Blood Oxygen Saturation ($SpO_2$). |
| **Accelerometer** | ADXL345 | 3-axis motion tracking for activity monitoring and fall detection. |
| **Temperature Sensor** | DS18B20 | Measures real-time body temperature. |
| **Local Display** | IPS TFT LCD Screen | Provides local, real-time visual readings for the user/caregiver. |
| **Power Supply** | 3.7V Li-Po Battery (150mAh) | Portable energy source with a Buck Converter (regulated to 3.3V). |

---

## 📊 Performance & Experimental Findings
The prototype was rigorously tested under laboratory environments against standard clinical tools, yielding highly reliable analytics:
* **Temperature Accuracy:** The DS18B20 sensor demonstrated an accuracy variance of only $\pm0.5^\circ\text{C}$.
* **Pulse & Oximetry:** The MAX30102 sensor achieved **95% accuracy** compared to commercial fingertip pulse oximeters.
* **Fall Detection:** The ADXL345 reliably identified normal motion at $>1.5\text{g}$ and logged critical fall instances at $>2.5\text{g}$ thresholds.

### Blynk Virtual Pin Mapping:
* `V0`: Temperature ($^\circ\text{C}$ or $^\circ\text{F}$)
* `V1`: Heart Rate (BPM)
* `V2`: Oxygen Saturation ($SpO_2$)
* `V3`: Motion Detection
* `V4`: Fall Detection
* `V5`: Emergency Alerts

---

## 🚀 Future Scopes
* Enhancing wearable ergonomics and battery longevity.
* Implementing advanced machine learning algorithms locally (Edge AI) for complex risk predictive analytics.
* Integrating mental health indices and environmental condition sensors.
