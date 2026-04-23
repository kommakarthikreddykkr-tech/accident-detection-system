# 🚗 Vehicle Accident Detection and Alert System

## 📌 Overview
This project is an **Arduino-based Vehicle Accident Detection System** that automatically detects accidents using a **MEMS accelerometer** and sends real-time alerts with location details using **GPS and GSM modules**.

The system helps in **quick emergency response** by notifying predefined contacts via SMS along with a Google Maps location link.

---

## ⚙️ Features
- 📡 Real-time accident detection using MEMS sensor  
- 📍 GPS-based location tracking  
- 📲 Automatic SMS alert using GSM module  
- 🔔 Buzzer alert for emergency indication  
- 📺 LCD display for system status  
- 🚨 Detects accident direction:
  - Left
  - Right
  - Front
  - Back

---

## 🧰 Components Used
- Arduino (Uno / Mega)  
- MEMS Accelerometer Sensor  
- GPS Module  
- GSM Module  
- 16x2 LCD Display  
- Buzzer  
- Motor (or LED for indication)  
- Push Button Switch  
- Power Supply  

---

## 🔌 Circuit Connections

| Component | Arduino Pin |
|----------|------------|
| LCD RS   | 8          |
| LCD EN   | 9          |
| LCD D4   | 10         |
| LCD D5   | 11         |
| LCD D6   | 12         |
| LCD D7   | 13         |
| GPS RX   | 3          |
| GPS TX   | 4          |
| Buzzer   | 7          |
| Motor    | 6          |
| MEMS X   | A0         |
| MEMS Y   | A1         |
| Switch   | 2          |

---

## 🧠 Working Principle
1. The MEMS sensor continuously monitors tilt values (X and Y axis).
2. If values exceed threshold → accident is detected.
3. Direction of accident is identified:
   - X-axis → Left / Right
   - Y-axis → Front / Back
4. System actions:
   - Activates buzzer  
   - Displays alert on LCD  
   - Sends SMS using GSM module  
5. GPS module provides location:
   - Latitude & Longitude  
   - Google Maps link  

---

## 📩 SMS Alert Example
RIGHT ACCIDENT
Vehicle Location Place
Latitude: 14.427856
Longitude: 77.704918
https://www.google.com/maps/place/14.427856,77.704918

Plz Rescue

---

## 🧪 Accident Detection Logic

| MEMS Values Condition | Result |
|----------------------|--------|
| Normal Range         | SAFE   |
| X decreases          | RIGHT ACCIDENT |
| X increases          | LEFT ACCIDENT  |
| Y decreases          | FRONT ACCIDENT |
| Y increases          | BACK ACCIDENT  |

---

## 🚀 How to Run
1. Connect all hardware components correctly  
2. Upload the Arduino code to the board  
3. Power ON the system  
4. Wait until GPS signal is acquired  
5. System starts monitoring automatically  

---

## 📁 Code Structure
- **Sensor Reading** → MEMS accelerometer values  
- **GPS Handling** → Location extraction  
- **GSM Communication** → SMS sending  
- **Display Module** → LCD updates  
- **Logic Control** → Accident detection  

---

## ⚠️ Notes
- Replace phone numbers in the code with your own  
- Ensure GSM SIM has sufficient balance  
- GPS may take time to lock initially  
- Adjust threshold values for better accuracy  

---

## 🔮 Future Improvements
- Mobile App integration  
- IoT cloud monitoring  
- Automatic emergency calling  
- AI-based accident prediction  
- Speed detection system  

---

## 👨‍💻 Author
**Karthik Reddy**
