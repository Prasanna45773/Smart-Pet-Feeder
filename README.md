# 🐾 Smart Pet Feeder Using ESP8266 and Blynk

An IoT-based Smart Pet Feeder that allows pet owners to remotely control food dispensing and monitor food levels using an ESP8266 NodeMCU, ultrasonic sensors, a servo motor, and the Blynk IoT platform.

## 📌 Project Overview

The Smart Pet Feeder is designed to make pet feeding more convenient. Two ultrasonic sensors monitor the food storage container and feeding bowl. Sensor readings are sent to the Blynk mobile application, allowing users to check food levels remotely and operate the servo-driven dispensing mechanism.

The system can also generate notifications when the food supply is low or the feeding bowl needs attention.

## ✨ Features

- **Remote Feeding Control:** Operate the dispenser through the Blynk application.
- **Food Level Monitoring:** Measure the distance to the food surface in the storage container.
- **Bowl Level Monitoring:** Monitor the food available in the feeding bowl.
- **Real-Time Updates:** Display sensor readings on the Blynk dashboard.
- **Food Alerts:** Notify users when food levels cross configured thresholds.
- **Serial Monitoring:** View sensor readings and system messages for debugging.

## 🛠️ Hardware Requirements

| Component | Quantity |
|---|---:|
| ESP8266 NodeMCU | 1 |
| HC-SR04 Ultrasonic Sensor | 2 |
| Servo Motor | 1 |
| Regulated 5V power supply | 1 |
| Jumper wires | As required |
| Breadboard | 1 |

## 🔌 Pin Configuration

| Component | Pin | NodeMCU Pin |
|---|---|---|
| Ultrasonic Sensor 1 | TRIG | D2 / GPIO4 |
| Ultrasonic Sensor 1 | ECHO | D1 / GPIO5 |
| Ultrasonic Sensor 2 | TRIG | D3 / GPIO0 |
| Ultrasonic Sensor 2 | ECHO | D4 / GPIO2 |
| Servo Motor | Signal | D7 / GPIO13 |
| Sensors | VCC | 5V supply |
| Sensors | GND | Common GND |

**Important:** The HC-SR04 Echo output is typically 5V, while ESP8266 GPIO pins operate at 3.3V. Use a suitable voltage divider or logic-level shifter for each Echo connection. Power the servo from a suitable external supply if needed and connect its ground to the NodeMCU ground.

## 💻 Software Requirements

- Arduino IDE
- ESP8266 board support package
- Blynk IoT account and mobile application
- ESP8266 Wi-Fi library
- Blynk library for ESP8266
- Servo library compatible with ESP8266

## ⚙️ Setup Instructions

1. Install the Arduino IDE and configure ESP8266 NodeMCU board support.
2. Install the required libraries.
3. Create a Blynk IoT template and device.
4. Configure the required virtual pins and event codes.
5. Open the project source file in Arduino IDE.
6. Configure your Wi-Fi credentials and Blynk authentication details securely.
7. Select the correct NodeMCU board and COM port.
8. Upload the code and open the Serial Monitor.
9. Connect the device to Wi-Fi and verify the sensor readings.
10. Open the Blynk application to monitor food levels and control the servo.

## 📱 Blynk Virtual Pin Configuration

| Virtual Pin | Purpose |
|---|---|
| V0 | Storage container distance |
| V1 | Storage status LCD widget |
| V2 | Servo angle control |
| V3 | Bowl status LCD widget |
| V4 | Feeding bowl distance |

Configure the LCD widgets and servo control in your Blynk dashboard to match the source code.

## 🔔 Notification Events

Configure these event codes in the Blynk template:

- `food_dispenser_low` — Food storage level is low.
- `food_bowl_empty` — Feeding bowl needs refilling.
- `food_bowl_full` — Bowl level meets the configured full-bowl threshold.

Notification thresholds must be calibrated according to the physical dimensions of the container and bowl.

## 🔐 Security

Do not upload your Wi-Fi password or Blynk authentication token to a public repository. Store credentials in a separate, ignored configuration file or provide them through a secure local configuration process.

If credentials have already been committed publicly, rotate them before publishing the updated project.

## 🚀 Future Enhancements

- Automatic scheduled feeding.
- Adjustable portion control.
- Food-level percentage indicators.
- Feeding history and usage statistics.
- Improved sensor error detection.
- Automatic feeding based on configurable food-level thresholds.

## 👨‍💻 Applications

- Smart pet care
- IoT-based home automation
- Remote pet feeding
- Embedded systems and sensor monitoring

## 📄 License

Choose an appropriate open-source license if you want others to reuse or modify this project.

---

**Project:** Smart Pet Feeder  
**Platform:** ESP8266 NodeMCU + Blynk IoT  
**Domain:** Internet of Things (IoT)
