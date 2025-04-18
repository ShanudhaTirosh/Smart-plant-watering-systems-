# 🌱 ESP8266 Smart Soil Moisture Control System

A sleek, IoT-powered smart irrigation system built using the **ESP8266 NodeMCU**, integrating a **soil moisture sensor**, **DHT11 temperature & humidity sensor**, **OLED display**, and **Blynk IoT** platform for real-time monitoring and control.

---

## ✨ Features

- 🚿 **Smart Water Pump Control** – automatic & manual modes
- 🌡️ **Temperature & Humidity Monitoring** – via DHT11/DHT22
- 🌍 **WiFi Connectivity** – setup via captive portal (WiFiManager)
- 📲 **Blynk IoT Integration** – live updates & remote control
- 🖥️ **OLED Display** – shows sensor readings and system status
- ♻️ **Watchdog Timer** – ensures system stability
- ⚠️ **Sensor Error Handling** – for DHT and moisture sensor

---

## ⚙️ Hardware Requirements

| Component              | Description                                |
|------------------------|--------------------------------------------|
| ESP8266 NodeMCU        | Microcontroller board                      |
| Soil Moisture Sensor   | Analog sensor for detecting moisture level |
| DHT11/DHT22            | For temperature and humidity               |
| OLED Display (SSD1306) | 128x64 I2C screen                          |
| Relay Module + Pump    | For controlling irrigation                 |
| Jumper wires & Breadboard | For connections                        |

---

## 🧠 Pin Configuration

| Component            | ESP8266 Pin |
|----------------------|-------------|
| Soil Moisture Sensor | A0          |
| Pump (via Relay)     | D5          |
| DHT Sensor           | D4          |
| OLED (SDA)           | D2 (GPIO4)  |
| OLED (SCL)           | D1 (GPIO5)  |

---

## 📲 Blynk Virtual Pins

| Virtual Pin | Function                        |
|-------------|----------------------------------|
| `V0`        | Soil Moisture (%)               |
| `V1`        | Temperature (°C)                |
| `V2`        | Humidity (%)                    |
| `V3`        | Manual Pump Control (Button)    |
| `V4`        | Mode Switch: Auto / Manual      |

---

## 🚀 Getting Started

1. **Install Libraries** via Arduino Library Manager:
   - `Blynk`
   - `WiFiManager`
   - `DHT sensor library`
   - `Adafruit GFX` & `Adafruit SSD1306`

2. **Configure Blynk**:
   - Create a template on [Blynk Cloud](https://blynk.cloud)
   - Replace the following in the code:
     ```cpp
     #define BLYNK_TEMPLATE_ID "YOUR_TEMPLATE_ID"
     #define BLYNK_TEMPLATE_NAME "YOUR_TEMPLATE_NAME"
     #define BLYNK_AUTH_TOKEN "YOUR_AUTH_TOKEN"
     ```

3. **Upload Code** to ESP8266 using Arduino IDE or PlatformIO

4. **WiFi Setup**:
   - On first boot, connect to `ESP-Config` hotspot
   - Enter your WiFi credentials

5. **Enjoy remote monitoring** through Blynk mobile app

---

## 🖼️ Preview

> *(Add screenshots or photos here)*  
> OLED Display | Blynk UI  
> ------------ | --------  
> ![OLED Example](https://via.placeholder.com/150x64?text=OLED+Preview) | ![Blynk UI](https://via.placeholder.com/150x300?text=Blynk+App+UI)

---

## 🧩 Future Enhancements

- 📦 Add soil **temperature sensor**
- 💧 Track **water usage**
- 🌐 Integrate with **Home Assistant** or **MQTT**
- 📈 Enable **data logging** to SD card or cloud

---

## 📝 License

This project is licensed under the **MIT License**.  
Feel free to fork, contribute, and customize!

---

## 🤝 Contributing

Pull requests and suggestions are welcome.  
Let's build smarter farms together!

---
