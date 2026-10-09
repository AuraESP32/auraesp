# AuraESP 🚀

**AuraESP** is a lightweight, multi-functional wireless command station firmware for the **ESP32**. It allows you to control wireless broadcasts, perform local Bluetooth Low Energy (BLE) reconnaissance, and monitor system diagnostics in real-time—all through a clean and responsive Arduino IDE **Serial Monitor** command-line interface.

---

## 🌟 Key Features

* **`/wifi <name>`**: Broadcasts an open Wi-Fi Access Point at maximum hardware transmit power (`19.5 dBm`) for maximum range.
* **`/viewwifi`**: Displays the currently active custom broadcast SSID and its network IP address.
* **`/bt <name>`**: Instantly spins up and broadcasts a custom Bluetooth classic/BLE device name.
* **`/signal`**: Scans nearby 2.4GHz BLE devices (such as AirPods, smart TVs, and beacons), listing their names, unique MAC addresses, and exact RSSI signal strength in dBm.
* **`/info`**: Prints real-time hardware metrics including uptime, free heap memory, CPU frequency, and wireless radio status.
* **`/stop`**: Instantly and gracefully terminates all active Wi-Fi and Bluetooth broadcasts.
* **`/help`**: Pulls up the built-in command list.

---

## 📦 Hardware Requirements

* **ESP32 Development Board** (ESP32-WROOM-32 or compatible variant with Bluetooth support).
* **Micro-USB / USB-C Cable** (A stable, high-quality cable is recommended to handle current spikes when broadcasting Wi-Fi at max power).

---

## 🛠️ Software & Libraries

Make sure you have the **ESP32 board package** installed in your Arduino IDE, along with these standard libraries (included with the ESP32 core):
* `WiFi.h`
* `BluetoothSerial.h`
* `BLEDevice.h`
* `BLEScan.h`
* `BLEAdvertisedDevice.h`

---

## ⚙️ Setup & Usage Instructions

1. Open the Arduino IDE and create a new sketch named `auraesp`.
2. Paste the source code from `auraesp.ino`.
3. Select your specific ESP32 board model and port under **Tools**.
4. Click **Upload** to flash the firmware.
5. Open the **Serial Monitor** and configure settings to:
   * **Baud Rate:** `115200`
   * **Line Ending:** `Newline` or `Both NL & CR`
6. Type `/help` to get started!

---

## 💻 Example Command Line Operations

```text
/wifi AuraNetwork
/bt AirPods Pro
/signal
/info
/viewwifi
/stop
