
# ESP-32 Necronomicon

An ESP32 multitool to do kool stuff, inspired by Futaba Sakura’s Persona.

---

## ⚠️ Disclaimer

This project is **currently in concept phase** and is intended for **educational and research purposes only**. The use of jamming or interference tools may be **illegal in your country**. Use responsibly and only on devices you own or have explicit permission to test.

---

## 🧰 Features

- Modular tool architecture (easy to add new tools)
- SSD1306 display support
- Built-in RF tools:
  - **Jammer** (BLE, 2.4GHz protocols)
  - **RF Scanner** (CC1101 frequency band)
  - **Packet Sniffer**
  - **RF Emulator/Replay**
  - **BLE Spammer** (ESP32 native BLE)
  - **Bad Portal**
  - **Singular Deauther** (ESP32 Wi-Fi)
- **SDHC module** for storing web pages and logs

---

## 🧩 Hardware Support

- **ESP32** (Node32s, Wemos D32, etc.)
- **CC1101** radio module (for sub-GHz RF)
- **SSD1306 OLED Display** (128x64 I2C/SPI)
- **SDHC module** to store Webserver pages and scanned frequencies
- **Push buttons** for menu navigation

---
## 🔌 Pin Diagram (NodeMCU-32S)

### ESP32 (NodeMCU-32S) + CC1101 (SPI)

| CC1101 | NodeMCU-32S Pin |
|--------|-----------------|
| VCC    | 3.3V            |
| GND    | GND             |
| MOSI   | GPIO 23         |
| MISO   | GPIO 19         |
| SCK    | GPIO 18         |
| CSN    | GPIO 5          |
| GDO0   | GPIO 27         |

### ESP32 (NodeMCU-32S) + SDHC Module (SPI)

| SDHC Module | NodeMCU-32S Pin |
|-------------|-----------------|
| VCC         | 3.3V / 5V (check module) |
| GND         | GND             |
| MOSI        | GPIO 13         |
| MISO        | GPIO 12         |
| CLK / SCK   | GPIO 14         |
| CS          | GPIO 25         |

### ESP32 (NodeMCU-32S) + SSD1306 (I2C)

| SSD1306 | NodeMCU-32S Pin |
|--------|-----------------|
| VCC    | 3.3V            |
| GND    | GND             |
| SDA    | GPIO 21         |
| SCL    | GPIO 22         |

### ESP32 (NodeMCU-32S) + Buttons

| Function | NodeMCU-32S Pin |
|----------|-----------------|
| Up       | GPIO 33         |
| Down     | GPIO 32         |
| OK       | GPIO 15         |
| Back     | GPIO 26         |
---

## 🛠️ Supported Tools

| Tool          | Description |
|---------------|-------------|
| BLE Jammer    | Jams Bluetooth Low Energy connections (ESP32 native) |
| Wi-Fi Deauther| Sends deauth packets to disconnect Wi-Fi clients (ESP32 native) |
| Bad Portal    | Hosts a fake captive portal (ESP32 native) |
| RF Scanner    | Scans for active RF signals via CC1101 |
| Packet Sniffer| Captures and analyzes RF packets via CC1101 |
| RF Emulator   | Replays captured RF signals via CC1101 |

---

## 🌐 Web Interface

The project includes an optional web server that allows you to control the device remotely:

- Live data visualization
- Tool configuration via browser
- REST API for external control
- WebSocket support for real-time updates

---

## 📁 Project Structure

```
ESP-32-Necronomicon/
│
├── Necronomicon.ino  # Main entry point
├── menu.h/cpp        # Menu interface logic
├── display.h/cpp     # OLED display handling
├── storage.h/cpp     # SDHC handling
├── tools/
│   ├── jammer.h/cpp
│   ├── scanner.h/cpp
│   ├── sniffer.h/cpp
│   ├── ble_spammer.h/cpp
│   ├── deauther.h/cpp
│   └── bad_portal.h/cpp
├── web/
│   ├── server.h/cpp
│   └── assets/       # HTML, CSS, JS files
└── README.md
```

---

## 🚧 Status

- **Phase**: Concept / Early Development
- This project is **not ready for production use**
- Contributions and testing are welcome
- APIs and features may change frequently

---

## 📋 Requirements

### Libraries
- `SPI`
- `Wire`
- `Adafruit_GFX`
- `Adafruit_SSD1306`
- `WebServer` (for web interface)
- `WiFi` (for Wi-Fi tools)
- `BLE` (for ESP32 BLE tools)
- `SD` (for SDHC storage)

---

## 🧪 Usage

1. Upload the firmware to your ESP32
2. Connect the CC1101 module, OLED display, SD card, and buttons
3. Power on and navigate using the buttons
4. Select tools from the main menu

---

## 🛡️ Legal Notice

The use of this software to interfere with wireless communications may violate local laws. Use only in controlled environments and for educational purposes.

---

## 🤝 Contributing

This project is in active development. Contributions are welcome! Please open an issue or submit a pull request.

---

## 📄 Credits

I would gladly appreciate if you credit me (@oscarpag) if you intend to include and/or modify parts of my project.  
Code and development is done by @oscarpag. I am an amateur, so errors may be included as I make strong use of AI coding agents.
