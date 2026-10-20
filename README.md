# Automatic Real-Time Monitoring System for Sustainable Energy Consumption

An IoT-based energy monitoring and load control project designed to monitor electrical parameters and support more efficient energy usage.

## Project Overview

This project uses an ESP32 microcontroller and a PZEM-004T energy meter to measure electrical parameters such as voltage, current, power, and energy consumption. The firmware is designed to send monitoring data to Firebase Realtime Database and support relay-based control of four loads.

A web dashboard provides the user interface for viewing and interacting with the monitoring system.

## Live Dashboard

[Open the Energy Monitoring Dashboard](https://iot-monitor-dashboard.netlify.app/)

## Key Features

- Monitoring of voltage, current, power, and energy consumption.
- ESP32-based data acquisition.
- Firebase Realtime Database integration in the firmware.
- Relay-based control for four loads.
- Web dashboard for monitoring and load-control interaction.

*Verify that each feature is working end-to-end in your current deployment before presenting it as a fully tested feature.*

## Hardware Components

- ESP32 development board
- PZEM-004T energy monitoring module
- Four-channel relay module
- Four test loads (bulbs)
- Appropriate power supply, wiring, and electrical protection

## Technologies Used

- **Embedded:** C++, Arduino framework, PlatformIO
- **Microcontroller:** ESP32
- **Energy Measurement:** PZEM-004T
- **Cloud Database:** Firebase Realtime Database
- **Dashboard:** Deployed web dashboard

## System Workflow

1. The PZEM-004T measures electrical parameters.
2. The ESP32 reads the measurements through serial communication.
3. The firmware prepares monitoring data for Firebase Realtime Database.
4. The relay-control logic switches the connected loads.
5. The web dashboard serves as the interface for monitoring and control.

## Repository Structure

- `src/main.cpp` — Main program and update loop
- `src/pzem_sensor.cpp` — Energy-meter reading logic
- `src/firebase_handler.cpp` — Wi-Fi, Firebase, and remote-control handling
- `src/relay.cpp` — Relay initialization and load-control functions
- `platformio.ini` — PlatformIO configuration

Required header files and the `.gitignore` should also be included.

## Setup

1. Install Visual Studio Code and the PlatformIO IDE extension.
2. Open the project directory in PlatformIO.
3. Install the required dependencies specified in `platformio.ini`.
4. Configure your Wi-Fi and Firebase credentials securely in the local configuration.
5. Connect the ESP32, PZEM-004T, and relay module according to the circuit and pin definitions.
6. Build and upload the firmware.
7. Verify sensor readings, Firebase updates, and relay operation.
8. Open the dashboard and verify its connection to the data source.

## Security

Do not commit Wi-Fi passwords, Firebase secrets, private keys, or other credentials. Keep sensitive configuration in local files excluded from Git.

## Project Status

Developed as an academic project focused on IoT-based electrical energy monitoring and load control.

## Author

Swathi Priya

[GitHub Profile](https://github.com/swathipriyas1205)
