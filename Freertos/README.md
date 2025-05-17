# FreeRTOS Project

This folder contains embedded system projects developed using the FreeRTOS real-time operating system.

## 🧠 What is FreeRTOS?
FreeRTOS is an open-source real-time operating system kernel for embedded devices that makes it easier to run multiple tasks concurrently using preemptive or cooperative multitasking.

## 🧰 Recommended Tools
- STM32CubeIDE (for STM32 + FreeRTOS)
- PlatformIO (ESP32 with Arduino/ESP-IDF + FreeRTOS)
- Keil MDK or MPLAB X (for other microcontrollers)
- FreeRTOS Kernel (https://github.com/FreeRTOS/FreeRTOS-Kernel)

## 📁 Typical Folder Structure
- `Core/` – Application code and FreeRTOS task logic
- `freertos/` – FreeRTOS kernel source (if not part of toolchain)
- `Inc/` – Header files
- `Src/` – Source files
- `Tasks/` – Task creation and logic
- `platformio.ini` – PlatformIO config (if using PlatformIO)

## 🔧 Features Implemented
- Task scheduling and management
- Queues and semaphores for inter-task communication
- Timers and delays using `vTaskDelay()`
- Interrupt-safe mechanisms
- CPU and memory utilization monitoring

## ▶️ How to Build and Run
### For STM32
1. Open the `.ioc` file with STM32CubeMX to regenerate code.
2. Import into STM32CubeIDE and build.
3. Connect your board and flash.

### For ESP32 (PlatformIO)
1. Open the folder in VS Code with PlatformIO.
2. Define FreeRTOS tasks in `src/main.cpp`.
3. Build and upload with PlatformIO.

## 📌 Notes
- Ensure config settings in `FreeRTOSConfig.h` are properly set for your MCU and clock.
- Use `uxTaskGetStackHighWaterMark()` to debug stack overflows.
- Use `vTaskSuspend()` and `vTaskResume()` carefully to manage task state.

## 📚 References
- [FreeRTOS Documentation](https://freertos.org)
- [STM32CubeMX + FreeRTOS Guide](https://www.st.com/en/development-tools/stm32cubemx.html)
- [ESP32 + FreeRTOS](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/system/freertos.html)

---

> ⚠️ Always monitor heap usage (`xPortGetFreeHeapSize()`) and avoid blocking tasks unnecessarily to maintain system responsiveness.
