# Esp-32-Necronomicon
An esp32 multitool to mess with people, inspired by Futaba Sakura’s Persona.

---

## ⚠️ Disclaimer

This project is **currently in concept phase** and is intended for **educational and research purposes only**. The use of jamming or interference tools may be **illegal in your country**. Use responsibly and only on devices you own or have explicit permission to test.

---

## 🧰 Features

- Modular tool architecture (easy to add new tools)
- SSD1306 display support
- Built-in RF tools:
  - **Jammer** (BLE, Wi-Fi, 2.4GHz)
  - **RF Scanner**
  - **Packet Sniffer**
  - **RF Emulator/Replay**
  - **BLE Spammer**
  - **Bad Portal**
  - **Singular Deauther**

---

## 🧩 Hardware Support

- **ESP32** (Node32s, Wemos D32, etc.)
- **CC1101** radio module
- **SSD1306 OLED Display** (128x64 I2C/SPI)
- **SDHC modules** to store Webserver pages and scanned frequencies
- **Push buttons** for menu navigation

---

## 🛠️ Supported Tools

| Tool          | Description |
|---------------|-------------|
| RF Jammer     | Jams BLE, Wi-Fi, or all 2.4GHz channels |
| RF Scanner    | Scans for active RF signals |
| Packet Sniffer| Captures and analyzes RF packets |
| RF Emulator   | Replays captured RF signals |
| BLE Spammer   | Sends BLE advertisements (ESP32 native BLE) |

---

## 🌐 Web Interface

The project includes an optional web server that allows you to control the device remotely:

- Live data visualization
- Tool configuration via browser
- REST API for external control
- WebSocket support for real-time updates

---

## 📁 Project Structure

RFToolkit/
│
├── RFToolkit.ino     # Main entry point
├── menu.h/cpp        # Menu interface logic
├── display.h/cpp     # OLED display handling
├── tools/
│   ├── jammer.h/cpp
│   ├── scanner.h/cpp
│   ├── sniffer.h/cpp
│   └── ...
├── web/
│   ├── server.h/cpp
│   └── assets/       # HTML, CSS, JS files
└── README.md

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
- `RF24`
- `Adafruit_GFX`
- `Adafruit_SSD1306`
- `WebServer` (for web interface)
- `BLE` (for ESP32 BLE tools)

---

## 🧪 Usage

1. Upload the firmware to your ESP32
2. Connect the radio module and OLED display
3. Power on and navigate using the buttons
4. Select tools from the main menu

---

## 🛡️ Legal Notice

The use of this software to interfere with wireless communications may violate local laws. Use only in controlled environments and for educational purposes.

---

## 🤝 Contributing

This project is in active development. Contributions are welcome! Please open an issue or submit a pull request.

---

##Credits
I would gladly appreciate if you credit me (@oscarpag) if you intend to include and/or modify parts of my project.
Code and developement is done by @oscarpag, i am an amateour so errors may be included as i make strong use of Ai coding agents.
