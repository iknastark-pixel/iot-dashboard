

# 📡 IoT-Based Environmental Monitoring System using ESP32 & MQTT

## 📌 Overview

This project is an IoT-based environmental monitoring system that uses an **ESP32 microcontroller** to collect real-time sensor data (temperature, humidity, and air quality) and transmit it to a remote server using the **MQTT protocol**.

The system is designed to demonstrate lightweight communication, real-time monitoring, and efficient data transmission in IoT applications.

---

## 🚀 Features

* 🌡️ Temperature & Humidity monitoring using DHT11 sensor
* 🌫️ Air quality detection using analog gas sensor
* 📶 WiFi-enabled data transmission via ESP32
* 📡 MQTT protocol for lightweight communication
* 🔁 Real-time data publishing
* ⚡ Low power and efficient system

---

## 🛠️ Technologies Used

* **Hardware:**

  * ESP32
  * DHT11 Sensor
  * Air Quality Sensor (Analog)
  * Breadboard & Jumper Wires

* **Software:**

  * Arduino IDE
  * Embedded C / Arduino Code
  * MQTT Protocol
  * WiFi Library

---

## 🔌 Hardware Connections

### DHT11 Sensor:

* VCC → 3.3V (ESP32)
* GND → GND
* Data → GPIO 4

### Air Quality Sensor:

* VCC → 3.3V / 5V
* GND → GND
* Analog Output → GPIO 34

---

## ⚙️ Working Principle

1. The ESP32 connects to a WiFi network.
2. Sensors (DHT11 and air sensor) collect environmental data.
3. The data is processed by the ESP32.
4. Using MQTT protocol:

   * ESP32 acts as a **publisher**
   * Sends data to an MQTT **broker**
5. The data can be viewed by any MQTT **subscriber** (dashboard/app).

---

## 📡 MQTT Configuration

* **Broker Address:** (e.g., test.mosquitto.org or your own server)
* **Port:** 1883 (default MQTT port)
* **Topics Used:**

  * `sensor/temperature`
  * `sensor/humidity`
  * `sensor/air_quality`

### Why Port 1883?

Port 1883 is the **default port for MQTT communication without encryption**, making it lightweight and ideal for IoT devices.

---

## 📂 Project Structure

```
📁 IoT-ESP32-MQTT-Project
 ├── 📄 README.md
 ├── 📄 main.ino
 ├── 📄 config.h
 └── 📁 images (optional)
```

---

## 🧑‍💻 Installation & Setup

### 1. Clone Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Open in Arduino IDE

* Install ESP32 board support
* Install required libraries:

  * WiFi.h
  * PubSubClient.h
  * DHT.h

### 3. Configure WiFi & MQTT

Update:

```cpp
const char* ssid = "YOUR_WIFI";
const char* password = "YOUR_PASSWORD";
const char* mqtt_server = "BROKER_ADDRESS";
```

### 4. Upload Code

* Select ESP32 board
* Upload code to ESP32

---

## 📊 Output

* Sensor data is continuously sent to MQTT broker
* Can be visualized using:

  * MQTT Explorer
  * Node-RED Dashboard
  * Mobile apps

---

## 🔄 Future Enhancements

* Add cloud integration (AWS / Firebase)
* Use secure MQTT (TLS – Port 8883)
* Add mobile/web dashboard
* Implement alerts (SMS/Email)
* Add more sensors

---

## 🧠 Concepts Used

* IoT Architecture
* MQTT Protocol (Publisher–Subscriber model)
* Wireless Communication (WiFi)
* Embedded Systems

---


---

## 📜 License

This project is open-source and available under the MIT License.

---

## 🙌 Acknowledgment

This project was developed as part of an academic IoT learning experience.


