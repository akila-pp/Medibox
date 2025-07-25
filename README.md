# Medibox
MediBox is a smart, IoT-enabled medicine dispensing system designed to help patients take their medications on time. Developed using the Wokwi simulation platform, it combines alarm-based scheduling, environmental sensing, and automated dispensing mechanisms to ensure proper medication management.



## 🛠 Features

-  **Alarm Management**: Set up to 2 daily alarms for medicine reminders.
-  **Buzzer & LED Alerts**: Alerts users when it’s time to take medication.
-  **Servo Motor Actuator**: Automatically opens the medibox compartment at alarm time.
- 🌡 **Temperature & Humidity Monitoring**: Ensures optimal storage conditions for medicines.
-  **IoT Integration via MQTT**:
  - Publishes temperature, humidity, and light intensity data.
  - Sends alarm schedules.
-  **Node-RED Dashboard**:
  - Live graph of environmental data.
  - Alarm visibility and parameter updates (like gamma, servo offset, etc.).
-  **OLED Display**:
  - Shows current time and sensor values.
  - Displays menu system for alarm and setting adjustments.
-  **User Interface**:
  - Four push buttons (UP, DOWN, OK, CANCEL) to navigate and control menu.
  - Menu includes:
    1. Set UTC Offset
    2. Set Alarm 1
    3. Set Alarm 2
    4. Enable/Disable Alarms
    5. View Active Alarms
    6. Delete Alarm

---

##  Hardware 

- ESP32 Dev Module
- DHT22 Temperature & Humidity Sensor
- LDR for light detection
- OLED Display (SSD1306 128x64)
- Servo Motor
- Buzzer
- Push Buttons (UP, DOWN, OK, CANCEL)
  

---

##  MQTT Topics

| Topic                              | Description                              |
|-----------------------------------|------------------------------------------|
| `medibox/220134K1_temp`           | Temperature data                         |
| `medibox/220134K1_humidity`       | Humidity data                            |
| `medibox/220134K1_light`          | Average light intensity                  |
| `medibox/220134K1_alarms`         | JSON array of active alarms              |
| `medibox/config/220134K1_ts`      | Sampling interval for light readings     |
| `medibox/config/220134K1_tu`      | Upload interval to MQTT                  |
| `medibox/config/220134K1_theta_offset` | Servo base angle                    |
| `medibox/config/220134K1_gamma`   | Light compensation factor                |
| `medibox/config/220134K1_T_med`   | Target temperature for environment logic |

---

##  Node-RED Dashboard

- Realtime data plotting (temperature, humidity, light)
- Visual display of current alarms
- Control panel to update configuration remotely via MQTT

---

