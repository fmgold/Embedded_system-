# ESP32 Project

This folder contains code for ESP32-based IoT and embedded system projects.

## Recommended Tools
- PlatformIO (VS Code) or Arduino IDE
- ESP-IDF (for advanced development)

## Folder Structure (PlatformIO Style)
- `src/` – Main application source files
- `include/` – Header files
- `lib/` – External libraries
- `data/` – SPIFFS/LittleFS content (if any)
- `platformio.ini` – Project configuration

## How to Build and Flash
1. Open the folder in VS Code with PlatformIO installed.
2. Edit `platformio.ini` as needed.
3. Use the PlatformIO build and upload buttons or `pio run --target upload`.

## Notes
Ensure your ESP32 board drivers are installed and the correct COM port is selected.
