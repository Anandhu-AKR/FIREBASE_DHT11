# 🌡️ ESP8266 DHT11 Firebase Logger

This project demonstrates reading temperature and humidity from a DHT11 sensor using an ESP8266 (e.g., NodeMCU) and uploading the data to Firebase Realtime Database.

---

## 💡 Features

- Reads **temperature** and **humidity** from DHT11 sensor.
- Uploads data to Firebase Realtime Database every 15 seconds.
- Uses **Firebase-ESP8266** library by Mobizt.

---

## 🛠️ Hardware Requirements

- ESP8266 development board (e.g., NodeMCU)
- DHT11 sensor
- Jumper wires
- Breadboard

---

## ⚙️ Software Requirements

- Arduino IDE
- [Firebase-ESP8266 library](https://github.com/mobizt/Firebase-ESP8266)
- DHT sensor library

---

## 🔌 Wiring

| DHT11 Pin | ESP8266 Pin |
|-------------|-------------|
| VCC         | 3.3V or 5V  |
| GND         | GND         |
| DATA        | D2 (GPIO4) |

---

## 🗺️ Schematic

![Schematic](schematic.png)

---

## 🚀 Getting Started

### 1️⃣ Set up Firebase

1. Go to [Firebase Console](https://console.firebase.google.com/).
2. Create a new project.
3. Enable **Email/Password Authentication** in Authentication > Sign-in method.
4. Create a user (email & password) for your ESP8266 to log in.
5. Go to Realtime Database and create a database in **test mode** (you can secure it later).
6. Copy your **Database URL** (e.g., `https://your-project-id.firebaseio.com/`).
7. Go to Project Settings > General > Get your **Web API Key**.

---

### 2️⃣ Configure the Code

Replace these placeholders in your code:

```cpp
#define WIFI_SSID "YOUR_WIFI_SSID"
#define WIFI_PASSWORD "YOUR_WIFI_PASSWORD"
#define API_KEY "YOUR_FIREBASE_API_KEY"
#define DATABASE_URL "YOUR_DATABASE_URL"
#define USER_EMAIL "YOUR_FIREBASE_USER_EMAIL"
#define USER_PASSWORD "YOUR_FIREBASE_USER_PASSWORD"

```
## 3️⃣ Install Required Libraries
In Arduino IDE, go to Library Manager:

- Install [**Firebase ESP8266**](https://github.com/mobizt/Firebase-ESP8266) by Mobizt.
- Install [**DHT sensor library**](https://github.com/adafruit/DHT-sensor-library) by Adafruit.

## 4️⃣ Upload
- Connect ESP8266 to your PC.
- Select the correct board and port in Arduino IDE.
- Upload the code.
- Open Serial Monitor at **115200 baud** to see status and debug logs.

## 📊 Firebase Data Structure Example
```yaml
DHT11
├── Humidity: 55.0
└── Temperature: 27.0
```

## 🛡️ Security Note
✅ Important: Avoid committing your real Wi-Fi credentials, API keys, and passwords to public repositories. Always use placeholders or environment variables.

## 🤝 Credits
- [**Firebase-ESP8266 library**](https://github.com/mobizt/Firebase-ESP8266) by Mobizt
- [**DHT sensor library**](https://github.com/adafruit/DHT-sensor-library) by Adafruit

## 📬 License
This project is open-source and free to use for educational and personal projects.