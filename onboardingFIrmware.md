 
# Firmware Onboarding Notes

## 1. Initial Setup

Begin with a very simple firmware exercise.

1. Load the **example “Blink” sketch** and compile it.
2. Upload it to a target board (either **Arduino Uno** or **ESP32**).

Once the program is running and **`LED_BUILTIN` is blinking**, proceed with version control.

Commit the project with an **initial commit**, following the instructions in both the **Git** and **GitHub onboarding sections**.

---

## 2. Clean the Blink Code

Remove any **magic numbers** from the code.

Create **descriptive constants** for:

* GPIO pin number
* Baud rate
* Other configuration values

Example concept:

```
const int LED_PIN = LED_BUILTIN;
const int SERIAL_BAUD = 115200;
```

Commit these changes with a **clear and descriptive commit message**.

---

## 3. Add a Serial Splash

Add a **startup splash message** to the serial monitor.

A good splash message typically includes:

* Program name
* Version number
* Compile date and time
* Hardware platform
* Author name
* License

Example:

```
Program: Blink Demo
Version: 0.1
Compiled: __DATE__ __TIME__
Hardware: ESP32
Author: <name>
License: <license>
```

Commit the changes with a **descriptive commit message**.

---

## 4. Remove Blocking Code

Refer to the **multitasking article**.

Refactor the code to remove any `delay()` calls and replace them with **`millis()`-based timing**.

This introduces **non-blocking execution**, which is essential for embedded systems.

Commit the changes.

---

# ESP32 Specific Steps

## 5. Install WiFi Manager

Install **WiFiManager** and follow the tutorial from Random Nerd Tutorials.

Once implemented, commit your changes.

---

## 6. Install OTA and Filesystem

Install:

* **ElegantOTA**
* **Filesystem support (SPIFFS or LittleFS)**

Follow the Random Nerd Tutorials guide.

Commit the changes.

---

## 7. Customize Access Point Name

If you have multiple ESP32 devices, customize the **Access Point name** using the **MAC address**.

Example concept:

```
DeviceName-<MAC>
```

Commit the changes.

---

## 8. Boot Button Interaction

Use the **boot button** as a user input device.

Introduce the **Daily Struggle library** examples to detect different button press types.

Report detected presses to the **serial monitor**.

Examples to detect:

* Single press
* Double press
* Triple press
* Long press

---

## 9. LED Control with Multitasking

Use the **Flasher class** from the multitasking article to control the blinking behavior of `LED_BUILTIN`.

Example use cases:

* **Long press** → Reset LED blink rate to default
* **Two quick presses** → Increase blink rate
* **Three quick presses** → Turn LED off
* **Four quick presses** → Turn LED on

Commit the implementation.

---

## 10. Web Interface

Install the **WebSockets library**.

Serve a **simple webpage** that includes:

* LED control button
* LED status indicator
* Microcontroller temperature indicator using:

```
temperatureRead()
```

---

## 11. Authentication and Authorization

Add two user roles:

### Administrator

Can:

* Change LED blink rate
* See LED status
* View device temperature

### Viewer

Can only:

* See LED blink rate
* See LED status
* View device temperature

Reference material:
[https://share.google/aimode/RUgmEVkFHLmJ3OcD3](https://share.google/aimode/RUgmEVkFHLmJ3OcD3)

---

# Networking Topics to Explore

## WiFi (LAN)

* Telnet
* TCP/IP

Check **mDNS** functionality.

---

## WiFi (WAN / Internet)

Learn how to use:

* **MQTT**

---

## Bluetooth

Explore:

* Classic Bluetooth
* **BLE (Bluetooth Low Energy)**

Study **ESP32 network topologies**.

Reference:
[https://share.google/aimode/gSkqUoT5SoNz5HD0Z](https://share.google/aimode/gSkqUoT5SoNz5HD0Z)

---

## ESP32 Hardware

Read an introductory article and the **Random Nerd Tutorials ESP32 pinout guide** to understand the available pins and their capabilities.

---
 
