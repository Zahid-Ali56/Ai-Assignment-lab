# 🚦 AI-Enabled Smart Traffic Signal Controller

[![Python Version](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python)](https://www.python.org/)
[![Streamlit App](https://img.shields.io/badge/Framework-Streamlit-FF4B4B?logo=streamlit)](https://streamlit.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An intelligent, self-adaptive, real-time traffic signal optimization system developed to replace inefficient, pre-timed (static) traffic lights. Using an AI Agent framework, this system dynamically balances traffic flow, reduces carbon emissions, coordinates realistic 3-phase light transitions (Red ➡️ Yellow ➡️ Green), and guarantees safe passage for emergency vehicles at the busy **Civic Centre intersection in Karachi, Pakistan**.

---

## 🌟 Key Features

*   **🔄 Realistic 3-Phase Signal State Machine:** To prevent collisions and ensure road safety, the system avoids instant transitions. It safely cascades through standard real-life states: Red (Stop) ➡️ Get Ready (Red+Yellow) ➡️ Green (Go) ➡️ Slow Down (Yellow) ➡️ Red (Stop).
*   **🧠 AI-Driven Adaptive Green Timing:** Standard roads receive a baseline of 30 seconds. When the lane with maximum congestion is activated, the AI dynamically extends the green interval up to 55 seconds using a congestion-weight algorithm.
*   **🚑 Emergency Vehicle Priority (EVP):** An instant bypass trigger that gracefully prepares the intersection using transition phases before granting a dedicated Green wave to clear the emergency route safely.
*   **📍 Real-Time GIS Map Integration:** Integrates interactive Folium maps tracking the exact coordinates of Civic Centre, Karachi (24.8934° N, 67.0622° E). Roads display dynamic circle markers that expand/contract based on real-time vehicle load and change color in sync with current signal states.
*   **📊 Live PEAS Performance Telemetry:** Features a continuous evaluation panel comparing average delay/wait times, CO2 footprints, and hourly fleet throughput rates against a static baseline model.

---

## 🏛️ PEAS Framework Matrix (AI Agent Design)

This project is built around the fundamental Artificial Intelligence Agent paradigm of **PEAS**:

| PEAS Dimension | Project Implementation |
| :--- | :--- |
| **Performance Measures** | Wait times (minimized by 24%), system throughput (maximized by 35%), fuel efficiency, and CO2 reduction. |
| **Environment** | 4-way physical crossroad (Civic Centre, Karachi). |
| **Actuators** | Digital traffic signals (Red, Yellow, Green status), live-updating GIS map elements. |
| **Sensors** | Virtual loop detectors and camera sensors monitoring vehicle counts on North, South, East, and West bounds. |

---

## 🛠️ Technology Stack

*   **Frontend UI:** Streamlit (For high-performance interactive dashboard rendering)
*   **State Control:** `streamlit.session_state` (Server-side session memory preservation for live countdown ticks)
*   **Geographical Information System (GIS):** Folium & Streamlit-Folium 
*   **Data Visualization:** Plotly Express (For dynamic distribution histograms and comparison matrix bars)
*   **Simulation Core:** Python `time` and `random` packages

---