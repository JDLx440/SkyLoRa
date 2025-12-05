
# Hardware Documentation

## Project Overview
This project implements a **LoRa-based ultra-long-range communication system** using Meshtastic nodes. The system consists of:
- **Ground Station A (Sender)**
- **Balloon Node (Relay)**
- **Ground Station B (Receiver)**

Each node uses **Seeed Studio XIAO ESP32-S3** microcontrollers paired with **Wio-SX1262 LoRa modules** for reliable communication.

---

## 1. Ground Station A – Sender Node
**Role:** Transmits messages to the Balloon Node.

### Components
- **Microcontroller:** Seeed Studio **XIAO ESP32-S3**
- **LoRa Module:** Seeed Studio **Wio-SX1262 Kit** (supports Meshtastic & LoRa/LoRaWAN)
- **Antenna:** Medium-gain LoRa antenna (approx. 3–5 dBi)
- **Connectivity:** USB Type-C cable
- **Host Device:** PC running Meshtastic Python CLI

### Configuration
- Flash **Meshtastic firmware** onto XIAO ESP32-S3.
- Set node role: **Standard Node**.
- Connect via **serial interface** to send messages using Meshtastic CLI.

---

## 2. Balloon Node – Relay Node
**Role:** Acts as a relay between Ground Station A and B, mounted on a weather balloon.

### Components
- **Microcontroller:** Seeed Studio **XIAO ESP32-S3**
- **LoRa Module:** Seeed Studio **Wio-SX1262 Kit**
- **Antenna:** Low-gain LoRa antenna (compact for weight reduction)
- **Power Supply:** LiPo battery (3.7V, 1000mAh)
- **Enclosure:** Lightweight 3D-printed housing
- **Lift Mechanism:** Weather balloon rated for payload weight

### Configuration
- Flash **Meshtastic firmware**.
- Set node role: **Relay Node**.
- Optimize for minimal weight and secure antenna placement.

---

## 3. Ground Station B – Receiver Node
**Role:** Receives messages relayed by the Balloon Node.

### Components
- **Microcontroller:** Seeed Studio **XIAO ESP32-S3**
- **LoRa Module:** Seeed Studio **Wio-SX1262 Kit**
- **Antenna:** Medium-gain LoRa antenna
- **Display:** OLED screen for real-time message visualization
- **Connectivity:** USB Type-C cable
- **Host Device:** PC or microcontroller for logging/display

### Configuration
- Flash **Meshtastic firmware**.
- Set node role: **Standard Node**.
- Configure OLED display for incoming message output.

---


