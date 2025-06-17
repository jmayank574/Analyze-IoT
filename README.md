# Smartmeter Analysis: Real-Time IoT Pipeline on Azure

This project demonstrates an end-to-end real-time data pipeline for IoT smart meters using Microsoft Azure. It simulates smart meter telemetry from 9 devices using Visual Studio and streams data through the Azure IoT ecosystem for live monitoring, storage, and alerting.

---

## 📡 Smart Meter Simulation

- **Simulated Devices**: 9 Smart Meters
- **Telemetry Data**:
  - `temperature` (°C)
  - `voltage` (V)
  - `timestamp` (ISO 8601 format)
- **Simulation Platform**: Visual Studio (C#)

---

## ⚙️ Azure Architecture Overview

1. **Device Provisioning Service (DPS)**  
   Automatically provisions simulated smart meters to the Azure IoT Hub.

2. **IoT Hub**  
   Acts as the central message ingestion point for telemetry data.

3. **Stream Analytics**  
   Processes incoming messages in real-time:
   - **Hot Path**: Streams live data to Power BI for monitoring.
   - **Cold Path**: Stores raw data in Azure Storage for historical analysis.

4. **Azure Storage Account**  
   Stores raw telemetry in a structured format.

5. **Azure Databricks**  
   Used for batch analytics, anomaly detection, and trend exploration.

6. **Azure Functions + Logic Apps (⚠ Alerting)**  
   - **Azure Function** triggers on abnormal telemetry (e.g., temperature spikes).
   - **Logic App** sends notifications (email, Teams, etc.) based on alerts.

---

## 📊 Live Dashboard

- Built with **Power BI**
- Displays:
  - Device-wise temperature and voltage trends
  - Real-time updates
  - Last-reported timestamps

---

## Project Architecture

![Smartmeter Architecture](https://github.com/user-attachments/assets/e0628d45-b91c-484e-83fe-734c737f988c)

## Link to IOT Device Simulator 

https://github.com/nilendra1988/IOTProject
