# 📢 Smart Notice Board System

A smart, cloud-connected digital notice board designed to replace traditional paper-based notice systems with real-time, remotely managed announcements.

The system uses an **ESP32**, **OLED displays**, **Firebase Realtime Database**, and a **web-based administration dashboard** to publish and display notices dynamically.

## 🚀 Features

* 📢 Real-time digital notice publishing
* 🔄 Firebase Realtime Database synchronization
* 🖥️ Web-based admin dashboard
* 📺 Smart TV / large-screen notice display support
* 📱 Department-specific notices
* 🏫 Separate displays for **CSE** and **ECE**
* 🌐 Remote notice management
* 🌦️ Weather information integration
* ⚡ ESP32-based embedded system
* 🔔 Automatic display updates without manual intervention

## 🏗️ System Architecture

```text
                    ┌──────────────────────┐
                    │   Admin Dashboard    │
                    │   Web Application    │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Firebase Realtime DB │
                    │      Cloud Layer     │
                    └───────┬───────┬──────┘
                            │       │
              ┌─────────────┘       └─────────────┐
              ▼                                   ▼
      ┌───────────────┐                   ┌───────────────┐
      │     ESP32     │                   │ Smart TV /    │
      │  Notice Node  │                   │ Web Display   │
      └───────┬───────┘                   └───────────────┘
              │
        ┌─────┴─────┐
        ▼           ▼
   ┌────────┐  ┌────────┐
   │ CSE    │  │ ECE    │
   │ OLED   │  │ OLED   │
   └────────┘  └────────┘
```

## 🧩 Hardware

* ESP32 Development Board
* OLED Display × 2
* USB Power Supply
* Connecting Wires
* Breadboard / Prototype Board

## 💻 Software & Technologies

| Component            | Technology                 |
| -------------------- | -------------------------- |
| Microcontroller      | ESP32                      |
| Database             | Firebase Realtime Database |
| Embedded Programming | Arduino C++                |
| Admin Dashboard      | Web Application            |
| Display              | OLED                       |
| Large Display        | Smart TV / Web Browser     |
| API Integration      | Weather API                |
| Cloud Communication  | Firebase                   |

## 📁 Project Structure

```text
Smart-Notice-Board/
│
├── firmware/
│   └── esp32_notice_board.ino
│
├── dashboard/
│   ├── index.html
│   ├── css/
│   └── js/
│
├── display/
│   └── smart_tv_display/
│
├── assets/
│   └── images/
│
├── README.md
└── LICENSE
```

## 🔄 How It Works

1. The administrator creates or updates a notice through the web dashboard.
2. The notice is stored in Firebase Realtime Database.
3. The ESP32 retrieves the latest notice data from Firebase.
4. The corresponding department notice is displayed on the OLED display.
5. The web-based display can simultaneously show notices on a Smart TV or larger screen.
6. Weather information can be retrieved through the integrated weather API.
7. Updates are reflected across connected displays in real time.

## 🔥 Firebase Data Flow

```text
Admin
  │
  ▼
Web Dashboard
  │
  ▼
Firebase Realtime Database
  │
  ├──────────────► ESP32 ───► CSE OLED
  │                    └────► ECE OLED
  │
  └──────────────► Web Display ───► Smart TV
```

## ⚙️ Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Smart-Notice-Board.git
cd Smart-Notice-Board
```

### 2. Configure Firebase

Create a Firebase project and enable **Realtime Database**.

Configure the Firebase credentials required by the ESP32 firmware and dashboard.

### 3. Configure ESP32

Open:

```text
firmware/esp32_notice_board.ino
```

Update:

```cpp
WIFI_SSID
WIFI_PASSWORD
FIREBASE_API_KEY
FIREBASE_DATABASE_URL
```

Upload the firmware to the ESP32 using Arduino IDE.

### 4. Configure Dashboard

Add the Firebase configuration to the dashboard and open the web application in a browser.

## 🖥️ Dashboard

The administration dashboard is designed to allow authorized users to:

* Create notices
* Update existing notices
* Remove notices
* Manage department-specific announcements
* Control displayed content
* Monitor the digital notice board

## 🌦️ Weather Integration

The system can retrieve weather information using a weather API and display relevant environmental information alongside announcements.

## 🎯 Use Cases

* Colleges and universities
* Schools
* Department notice boards
* Laboratories
* Offices
* Reception areas
* Public information displays

## 🔮 Future Enhancements

* 🔐 Admin authentication and role-based access
* 📲 Mobile application
* 🔔 Push notifications
* 🖼️ Image and poster support
* 🎥 Video announcements
* 📊 Analytics for notice views
* 🗣️ Text-to-speech announcements
* 🤖 AI-assisted notice generation
* 🔌 OTA firmware updates
* 📡 Improved offline functionality

## 👨‍💻 Project

**Smart Notice Board System**

An IoT-based digital communication platform developed to provide centralized, real-time, and remotely managed announcements.

## 📄 License

This project is intended for educational and demonstration purposes.

---

⭐ If you find this project useful, consider giving the repository a star.
