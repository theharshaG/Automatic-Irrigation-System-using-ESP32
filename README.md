# Automatic-Irrigation-System-using-ESP32

##  Project Overview
This project is an automatic irrigation system built using ESP32, a soil moisture sensor, and a relay module.
The system monitors soil moisture levels and automatically turns a water pump ON or OFF based on soil condition.

##  Features
- Reads soil moisture using analog input
- Detects whether soil is DRY or WET
- Automatically controls water pump using relay
- Displays real-time data in Serial Monitor
- Fully automatic watering system

## 🛠 Components Used
- ESP32
- Soil Moisture Sensor (Analog Output)
- Relay Module (Active LOW)
- Water Pump
- External Power Supply (5V/12V for pump)
- Connecting wires

## Pin Configuration
 Component----> ESP32 Pin 
 Soil Sensor AO---->GPIO 34 
 Relay IN---->PIO 26 
 
##  How It Works
1. The soil sensor measures moisture level.
2. ESP32 reads analog value (0–4095).
3. If value > 2500 → Soil is DRY → Pump turns ON.
4. If value ≤ 2500 → Soil is WET → Pump turns OFF.
5. The system checks every 2 seconds.
   
## Logic Use

if (soilValue > 2500) {
    digitalWrite(relayPin, LOW);   // Pump ON
} else {
    digitalWrite(relayPin, HIGH);  // Pump OFF
}

## Author
Harsha G
Embedded Systems & IoT Learner 
