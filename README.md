# GPS TRACKER
[![Firmware](https://img.shields.io/badge/Firmware-View%20Code-green?style=for-the-badge&logo=github)](https://github.com/reihakuro/gps-tracker)
[![Dashboard](https://img.shields.io/badge/Dashboard-View%20Code-orange?style=for-the-badge&logo=github)](https://github.com/reihakuro/gps-tracker-web)

A complete IoT ecosystem designed for real-time location tracking and safety.

## 🗂️ Project Structure

This is a Master Repository, see detail information:
- [Firmware](https://github.com/reihakuro/gps-tracker): C++/PlatformIO source code for ESP32.
- [Dashboard](https://github.com/reihakuro/gps-tracker): JS/Vite source code for the monitoring dashboard.

## ✨ Features
### Tracking & Sensing
WiFi-Based Geolocation: Estimates location by scanning MAC addresses, useful for indoor/urban areas where GPS signal is weak.

- Motion Dynamics: Analyzes acceleration and tilt angles using the MPU6050 sensor.

- Fall Detection: Instant emergency alerts triggered by specific motion patterns.

### Monitoring & Control
- Live Dashboard: High-fidelity Leaflet maps with intelligent routing.

- Remote Response: Trigger a physical buzzer on the device via the web interface to locate the vehicle.

- Historical Logs: Export travel history and incident reports to Excel.

- Multi-language: Seamless switching between English and Vietnamese (i18n).

## 🏗️ System Architecture
The project built as a system where the hardware and software communicate asynchronously through the cloud.

- Firmware (Edge): Collects motion data (MPU6050) and scans nearby WiFi networks to estimate location via Geolocation APIs.

- Cloud (Bridge): Firebase Realtime Database acts as the central hub for data persistence and synchronization.

- Web Dashboard (User): Visualizes live location on Leaflet maps and manages emergency notifications.
