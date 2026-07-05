# IoT-Based Water Monitoring System

![Complete Prototype](images/prototype.jpg)
_(Placeholder: Upload Fig 4.13 Complete Prototype here)_

## Overview

The "IoT-Based Water Monitoring System" is a smart, real-time water management solution designed to track, measure, and control water usage efficiently. Built using an ESP32 microcontroller and a water flow sensor, this system continuously captures water flow rates and transmits the data to the ThingSpeak IoT platform via Wi-Fi. It provides a modern alternative to traditional, inefficient water management methods in residential apartments, industries, and agricultural fields.

## System Architecture

The system monitors water flow between the overhead tank and the end user, processing the data through an ESP32 and sending it to a cloud server for real-time visualization.

![Block Diagram](images/block_diagram.png)
_(Placeholder: Upload Fig 3.11 Block Diagram here)_

![Flowchart](images/flowchart.png)
_(Placeholder: Upload Fig 3.29 Flowchart here)_

## Key Features

- **Real-Time Monitoring:** Tracks the rate of water usage and total volume consumed in real time.
- **Leak Detection & Alerts:** Identifies unusual water usage patterns or undetected leaks to prevent water wastage and property damage.
- **Accurate & Fair Billing:** Monitors individual consumption to calculate precise billing costs.
- **Cloud Analytics & Dashboard:** Uses the ThingSpeak platform to display data trends, consumption graphs, and historical logs.
- **Sustainable Power:** The system operates on a 5V Lithium-ion battery recharged by a 5V solar panel, ensuring continuous operation.

## Hardware Components

- **Microcontroller:** ESP32 DevKit V1
- **Sensor:** Water Flow Sensor (5-10V)
- **Pump:** Diaphragm Water Pump (R385 6-12V)
- **Power Supply:** 1Ah Lithium-Ion Battery
- **Renewable Power Source:** 5V Solar Panel
- **Charging Module:** 5V 1A Type-C USB 18650 TP4056 Lithium Battery Charger

## Dashboard & Results

Users and administrators can access the ThingSpeak dashboard to view the Rate of Flow, Total Amount of Water Consumed, and Billing Amount.

![ThingSpeak Outcome](images/thingspeak_outcome.png)
_(Placeholder: Upload Fig 4.14 Thingspeak Outcome here)_

_(A live channel for this project can be viewed at [thingspeak.mathworks.com/channels/2621004](https://thingspeak.mathworks.com/channels/2621004))._

## Setup Instructions

1. Clone this repository to your local machine.
2. Open the `flowsensor_code.ino` file in the Arduino IDE.
3. Install the required libraries (`WiFi`, `Wire`, `ThingSpeak`) via the Arduino Library Manager.
4. Update the code with your specific network and ThingSpeak credentials:
   - `const char *ssid = "YOUR_WIFI_SSID";`
   - `const char *pass = "YOUR_WIFI_PASSWORD";`
   - `const char * myWriteAPIKey = "YOUR_THINGSPEAK_API_KEY";`
   - `unsigned long myChannelNumber = YOUR_CHANNEL_NUMBER;`
5. Compile and upload the code to your ESP32 board.
6. Connect the Flow Sensor's data pin to GPIO 13 on the ESP32.

## Contributors

- **Prajwal M** / [PRAJWAL0513](https://github.com/PRAJWAL0513)
