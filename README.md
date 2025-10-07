# 🔊 Voice-Activated Emergency Alert System

A **voice-controlled IoT safety device** designed to instantly alert emergency contacts when the user says **“Help Me”** — ensuring rapid response and peace of mind in critical situations.

---

##  Overview

The **Voice-Activated Emergency Alert System** is a compact, portable safety device built to detect a voice command and send an emergency SMS to predefined contacts.  
It combines **edge computing**, **machine learning**, and **GSM-based communication** for immediate and reliable alerts without requiring an internet connection.

---

## ⚙️ System Architecture

The system consists of three main modules that work together seamlessly:

1. **Arduino Nano 33 BLE**  
   - Performs voice recognition using on-board microphone  
   - Runs an embedded ML model built with **Edge Impulse**  
   - Handles command processing and control logic  

2. **GSM SIM900 Module**  
   - Sends SMS messages to pre-configured emergency contacts  
   - Operates on standard GSM networks  
   - Uses hardware serial communication  

3. **Voltage Level Shifter**  
   - Converts 3.3V ↔ 5V logic levels between Nano BLE and GSM module  
   - Protects hardware components from voltage mismatches  

---

## 🧩 Core Components

| Component | Description |
|------------|-------------|
| **Arduino Nano 33 BLE** | Edge computing microcontroller with integrated microphone |
| **GSM SIM900 Module** | For SMS-based emergency communication |
| **Voltage Level Shifter** | Ensures safe logic-level conversion |
| **SIM Card (with SMS plan)** | Enables mobile network connectivity |
| **Power Source (Li-ion Battery)** | Makes the system portable |

---

## 🧬 Machine Learning Model (Edge Impulse)

The **Edge Impulse** platform was used for:

- **Data Acquisition:** Capturing and labeling “Help Me” audio samples  
- **Model Training:** Building a neural network to detect the phrase  
- **Hyperparameter Tuning:** Optimizing performance and reducing false triggers  
- **Testing:** Ensuring robust recognition in noisy environments  

Once trained, the model was deployed directly to the **Nano 33 BLE** for **on-device inference**.

---

## 🔁 How It Works

1. **Voice Activation:**  
   The user says “Help Me”.

2. **Processing:**  
   The Nano 33 BLE detects the voice command using the trained Edge Impulse model.

3. **Alert Transmission:**  
   The GSM SIM900 module sends an SMS alert to the preset contact numbers.

4. **Notification:**  
   The contact receives the emergency message instantly.

---

## ⚡ Features

- Voice command activation (“Help Me”)  
- Instant SMS alerts to emergency contacts  
- Fully offline – no Wi-Fi or internet required  
- Compact, portable design  
- On-device AI with Edge Impulse  

---

## 🔧 Future Enhancements

-  **GPS Integration:** Include location data in the SMS alert  
-  **Power Optimization:** Extend battery life for longer operation  
-  **Wearable Design:** Miniaturize into a wristband or pendant form  
-  **Multi-Platform Alerts:** Expand notifications to mobile apps and email  

---

## 🧰 Software & Tools

| Tool | Purpose |
|------|----------|
| **PlatformIO** | Firmware development |
| **Edge Impulse Studio** | Data collection and model training |
| **Serial Monitor** | Debugging and serial communication |
| **GSM Library** | SMS functionality integration |

---

## ⚙️ Setup Instructions

1. **Collect and Train Voice Data**
   - Use Edge Impulse to record and label the phrase “Help Me”.
   - Train and deploy the model to Arduino Nano 33 BLE.

2. **Hardware Setup**
   - Connect GSM SIM900 module to Nano BLE via level shifter.  
   - Insert a SIM card with SMS capabilities.  
   - Power the device using a Li-ion battery.

3. **Upload Firmware**
   - Use pltformIO to flash the main code to Nano 33 BLE.
   - Ensure correct serial port and board are selected.

4. **Test System**
   - Speak “Help Me” near the device.
   - Confirm that the GSM module sends an SMS alert.

---

<img width="967" height="795" alt="image" src="https://github.com/user-attachments/assets/3f85aa42-7d51-4b34-9378-aaa33c02d98f" />
