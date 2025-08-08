# Wireless-Communication-Over-LoRaWAN-Using-STM32-Microcontroller

## Abstract
This project proposes a **LoRaWAN-based wireless communication system** using the STM32 microcontroller for data collection and transmission. Leveraging the **long range** and **low power** features of LoRaWAN, this system addresses the limitations of traditional wireless technologies in embedded applications. The system consists of **sensors**, a **LoRaWAN gateway**, and a **cloud platform** for **real-time environmental monitoring**.

---

## Problem Statement
Traditional wireless devices face challenges in **long-range real-time data transmission** while maintaining **reliability** and **energy efficiency**. For applications requiring remote monitoring, scalable and efficient communication systems are essential to enable accurate and timely data collection.

---

## Objectives
- Develop a **sensor node** integrated with STM32 to collect environmental data.
- Implement a **LoRaWAN transceiver module** to wirelessly transmit sensor data.
- Configure the **LoRaWAN gateway** to send data to the cloud for real-time visualization.

---

## Literature Review

### 4.1 Introduction to LoRaWAN and STM32 Nucleo WL55JC1
- **LoRaWAN** is a low-power, long-range protocol ideal for IoT.
- Works in unlicensed frequency ranges → cost-effective & scalable.
- **STM32 Nucleo WL55JC1** integrates STM32WL55 microcontroller with an ARM Cortex-M4 core and a built-in LoRa transceiver → compact, easy to develop, ideal for IoT applications like:
  - Industrial IoT
  - Smart Agriculture
  - Environmental Monitoring

### 4.2 Capabilities of STM32 Nucleo WL55JC1 in LoRaWAN Applications
- **Integrated LoRa Transceiver** → reduces power consumption and hardware complexity.
- **Dual-Core Architecture** (Cortex-M4 & Cortex-M0+) → performance + energy efficiency.
- **Low Power Modes** → ideal for battery-powered devices.
- **Development Support** → STM32CubeWL software package & STM32CubeMX tool.

### 4.3 Integration with Environmental Monitoring Systems
- Supports **I2C, SPI, UART** for sensor integration.
- Onboard data pre-processing reduces LoRaWAN network load.
- LoRaWAN stack meets LoRa Alliance requirements.
- Supports **Adaptive Data Rate (ADR)** to optimize power and range.
- Easily integrates with **AWS IoT, ThingsBoard, TTN**.

### 4.4 Applications in Similar Projects
- **Environmental Monitoring** → air quality & weather tracking.
- **Smart Agriculture** → soil moisture, temperature, light monitoring.
- **Industrial IoT** → equipment health monitoring.

---

## Methodology

### 5.1 Project Planning & Requirements
- **Hardware**: STM32 WL55 microcontroller, integrated LoRa module, sensors (DHT11, IR).
- **Software**: STM32Cube IDE, LoRaWAN libraries.

### 5.2 System Design
- **Architecture**:
  - STM32 WL55 for data processing & control.
  - LoRa module for long-range wireless communication.
  - Sensors for data collection.
  - Gateway → Cloud → Dashboard.
- LoRaWAN protocol for wide-area communication.

### 5.3 Software Development
- **Firmware**: Written in STM32Cube IDE.
- LoRaWAN configuration: frequency, data rate, payload size.
- Sensor integration: DHT11 (Temperature/Humidity), IR (Distance).
- Communication: Encode data, send packets, handle ACK/retransmissions.
- Cloud: Integrated with **The Things Network (TTN)** for real-time visualization.

### 5.4 Hardware Implementation
- STM32 WL55 + integrated LoRa module.
- Power via Serial wire (no external battery).
- Circuit designed to connect sensors with STM32.

### 5.5 Integration & Testing
- Unified hardware + software system.
- Data transmission tested between STM32 and LoRa module.
- LoRaWAN gateway configured for TTN.

---

## System Implementation Steps
1. **Sensor Data Acquisition**  
   - DHT11 → Temperature & Humidity.
   - IR sensor → Object distance.  
   - Data stored in variables & processed before transmission.

2. **LoRaWAN Data Transmission**  
   - Encode and send sensor data to LoRaWAN gateway.
   - Gateway → TTN → Dashboard.

3. **Cloud Dashboard**  
   - Real-time data visualization via TTN Application Server.

---

## Hardware Components
- STM32 Nucleo WL55JC1
- DHT11 Sensor
- IR Sensor
- LoRaWAN Gateway
- Serial wire for power

---

## Software & Tools
- STM32Cube IDE
- STM32CubeWL LoRaWAN libraries
- The Things Network (TTN)
- JSON for cloud data formatting

---

## System Architecture Diagram
*(Add diagram here if available)*

---

## Features
- Low power, long-range wireless communication.
- Real-time environmental monitoring.
- Scalable for various IoT applications.
- Easy integration with cloud platforms.

---

## Future Improvements
- Add more environmental sensors (CO₂, PM2.5, etc.).
- Implement battery power & solar charging.
- Improve security with encrypted LoRaWAN communication.

---

