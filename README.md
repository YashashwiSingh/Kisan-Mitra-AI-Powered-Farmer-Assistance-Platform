<div align="center">

# 🌾 Kisan Mitra
### *AI-Powered Farmer Assistance Platform*

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![AI Powered](https://img.shields.io/badge/AI-Powered-FF6B35?style=for-the-badge&logo=openai&logoColor=white)]()
[![Agriculture](https://img.shields.io/badge/Domain-AgriTech-4CAF50?style=for-the-badge)]()
[![Status](https://img.shields.io/badge/Status-Completed-22C55E?style=for-the-badge)]()
[![Timeline](https://img.shields.io/badge/March_2025-August_2025-FFC107?style=for-the-badge)]()

<br/>

> **Kisan Mitra** ("Farmer's Friend") is an AI-driven platform built to bridge the information gap between Indian farmers and the data they need to grow smarter.  
> It delivers **real-time groundwater levels**, **live crop market prices**, **weather forecasts**, and **personalized crop recommendations** — all tailored to a farmer's specific soil quality, water availability, and local climate.

<br/>

```
सही फसल · सही समय · सही जानकारी
Right Crop · Right Time · Right Information
```

</div>

---

## 📌 Table of Contents

- [The Problem](#-the-problem)
- [The Solution](#-the-solution)
- [Key Features](#-key-features)
- [System Architecture](#-system-architecture)
- [Feature Deep Dive](#-feature-deep-dive)
  - [Groundwater Monitoring](#-groundwater-level-monitoring)
  - [Crop Market Prices](#-crop-market-prices)
  - [Weather Intelligence](#-weather-intelligence)
  - [Crop Recommendations](#-personalized-crop-recommendations)
  - [Irrigation Management](#-irrigation-management-system)
- [AI & ML Pipeline](#-ai--ml-pipeline)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Impact & Use Cases](#-impact--use-cases)
- [Roadmap](#-roadmap)

---

## 🚜 The Problem

Indian farmers — who make up over **40% of the workforce** — face a daily battle against information asymmetry:

| Challenge | Impact |
|-----------|--------|
| 📉 **No visibility into market prices** | Selling crops far below fair value to middlemen |
| 💧 **Unmonitored groundwater depletion** | Over-irrigation leading to water table collapse |
| 🌦️ **No localized weather forecasts** | Crop loss from unpredicted weather events |
| 🌱 **Generic crop advice** | Wrong crops for local soil and climate conditions |
| 🔄 **Reactive irrigation** | Watering on instinct rather than actual water data |

---

## 💡 The Solution

Kisan Mitra puts a **precision agriculture assistant** in every farmer's hands — combining real-time environmental data with AI-driven personalization to help make decisions that directly protect crop yield and income.

Rather than generic advice, the platform reasons about **this farmer's land**, **this soil type**, **this water table level**, and **this week's weather** to deliver recommendations that are actually actionable.

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 💧 **Groundwater Monitoring** | Real-time groundwater level data to guide irrigation decisions |
| 📈 **Crop Market Prices** | Live mandi (market) price updates for informed selling decisions |
| 🌤️ **Weather Intelligence** | Hyperlocal weather forecasts and alerts for the farm's location |
| 🌾 **Crop Recommendations** | AI-personalized crop suggestions based on soil, water, and climate |
| 🚿 **Irrigation Management** | Smart irrigation scheduling based on actual groundwater data |
| 🗣️ **Regional Language Support** | Designed for accessibility in local Indian languages |

---

## 🏗 System Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                        Data Ingestion Layer                     │
│                                                                 │
│  ┌─────────────────┐  ┌──────────────────┐  ┌───────────────┐  │
│  │  Groundwater     │  │  Crop Market     │  │  Weather      │  │
│  │  Sensors / API  │  │  Price APIs      │  │  APIs         │  │
│  │  (Water table   │  │  (Mandi prices,  │  │  (Forecast,   │  │
│  │   depth data)   │  │   MSP data)      │  │   rainfall)   │  │
│  └────────┬────────┘  └────────┬─────────┘  └───────┬───────┘  │
│           └────────────────────┼────────────────────┘          │
└────────────────────────────────┼────────────────────────────────┘
                                 ▼
┌─────────────────────────────────────────────────────────────────┐
│                        AI Processing Layer                      │
│                                                                 │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │                  Recommendation Engine                   │  │
│  │                                                          │  │
│  │  Input: Soil Quality + Water Availability + Climate      │  │
│  │           + Market Prices + Weather Forecast             │  │
│  │                         ↓                                │  │
│  │            AI Crop Suitability Scoring                   │  │
│  │                         ↓                                │  │
│  │     Personalized Crop + Irrigation Recommendations       │  │
│  └──────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────┘
                                 ▼
┌─────────────────────────────────────────────────────────────────┐
│                         Farmer Interface                        │
│                                                                 │
│   📱 Mobile App / Web Dashboard                                 │
│   ├─ Groundwater level gauge & trend chart                      │
│   ├─ Today's mandi prices by crop and region                    │
│   ├─ 7-day weather forecast with farming advisories             │
│   ├─ Recommended crops ranked by suitability score             │
│   └─ Irrigation schedule with on/off alerts                     │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🔍 Feature Deep Dive

### 💧 Groundwater Level Monitoring

One of the most critical and underserved needs in Indian agriculture — knowing **how much water is actually available underground** before planning irrigation or crop selection.

```
Groundwater Sensors / Government API
            ↓
    Real-time depth readings
            ↓
    Trend Analysis (rising / falling / stable)
            ↓
    ┌──────────────────────────────┐
    │  Alerts & Advisories         │
    │  • "Water table critically   │
    │    low — switch to drought-  │
    │    resistant crops"          │
    │  • "Safe to irrigate today"  │
    └──────────────────────────────┘
```

**Why it matters:** Groundwater depletion is irreversible in the short term. Kisan Mitra helps farmers understand and respond to their local water table before it's too late.

---

### 📈 Crop Market Prices

Real-time **mandi (wholesale market) prices** for all major crops, updated continuously so farmers know the right time to sell.

| Data Point | Source |
|------------|--------|
| Current mandi price (₹/quintal) | Live market feeds |
| MSP (Minimum Support Price) | Government data |
| Price trend (7-day, 30-day) | Historical analysis |
| Nearby market comparison | Multi-mandi aggregation |

**Impact:** Farmers can choose *when* to sell and *which market* to sell at — avoiding the information gap that middlemen exploit.

---

### 🌤️ Weather Intelligence

Hyperlocal weather data tailored to the **farm's exact coordinates**, not just the nearest city:

- 🌧️ **Rainfall forecasts** — plan irrigation and harvesting around rain
- 🌡️ **Temperature alerts** — frost warnings, heat stress advisories
- 💨 **Wind advisories** — timing for pesticide spraying
- ⛅ **7-day outlook** — weekly farming activity planner

---

### 🌾 Personalized Crop Recommendations

The AI engine takes the farmer's specific conditions as input and ranks crops by suitability:

```
Farmer Profile Input:
├─ Soil Type (sandy / loamy / clay / black cotton)
├─ Soil pH and nutrient levels
├─ Current groundwater depth
├─ Water availability (irrigated / rain-fed)
├─ Location and historical climate
└─ Season / planting window

            ↓  AI Recommendation Engine

Output: Ranked crop list
├─ 🥇 Wheat         — Score: 94% — High market demand, suits soil
├─ 🥈 Mustard       — Score: 87% — Low water requirement
├─ 🥉 Chickpea      — Score: 79% — Drought-tolerant, good MSP
└─ ⚠️ Rice          — Score: 31% — NOT recommended (water table low)
```

---

### 🚿 Irrigation Management System

Smart irrigation scheduling powered by actual groundwater data — not guesswork:

```
Groundwater Level Data
        +
Crop Water Requirement (by growth stage)
        +
Weather Forecast (expected rainfall)
        ↓
Optimal Irrigation Schedule
├─ Next irrigation: Thursday, 6 AM
├─ Duration: 45 minutes
├─ Skip if: rainfall > 15mm predicted
└─ Alert: Groundwater low — reduce frequency
```

This prevents both **under-watering** (crop stress) and **over-watering** (water table depletion and root rot).

---

## 🤖 AI & ML Pipeline

```
┌──────────────────────────────────────────────────────────────┐
│                    Kisan Mitra AI Engine                     │
│                                                              │
│  Input Features:                                             │
│  ┌────────────────────────────────────────────────────────┐ │
│  │ soil_type · soil_ph · nutrient_npk · groundwater_depth │ │
│  │ water_availability · location · season · climate_zone  │ │
│  │ historical_rainfall · current_market_prices            │ │
│  └────────────────────────────────────────────────────────┘ │
│                           ↓                                  │
│  ┌──────────────────────────────────────────────────────┐   │
│  │              Crop Suitability Model                  │   │
│  │  • Scores each crop against farmer's conditions      │   │
│  │  • Weights market price attractiveness               │   │
│  │  • Penalizes water-intensive crops in drought areas  │   │
│  └──────────────────────────────────────────────────────┘   │
│                           ↓                                  │
│  ┌──────────────────────────────────────────────────────┐   │
│  │             Irrigation Scheduler                     │   │
│  │  • Calculates crop water demand by growth stage      │   │
│  │  • Cross-references groundwater availability         │   │
│  │  • Adjusts for forecasted rainfall                   │   │
│  └──────────────────────────────────────────────────────┘   │
│                           ↓                                  │
│             Personalized Farmer Advisory                     │
└──────────────────────────────────────────────────────────────┘
```

---

## 🛠 Tech Stack

| Technology | Role |
|------------|------|
| ![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white&style=flat) | Backend processing and AI pipeline |
| ![AI/ML](https://img.shields.io/badge/-AI_/_ML_Models-FF6B35?style=flat) | Crop recommendation and suitability scoring |
| ![Weather API](https://img.shields.io/badge/-Weather_APIs-4A90D9?style=flat) | Hyperlocal weather data ingestion |
| ![Market Data](https://img.shields.io/badge/-Market_Price_APIs-F7931E?style=flat) | Live mandi and MSP price feeds |
| ![Groundwater API](https://img.shields.io/badge/-Groundwater_Sensors_/_API-22C55E?style=flat) | Real-time water table data |
| ![Mobile](https://img.shields.io/badge/-Mobile_/_Web_Interface-3DDC84?logo=android&logoColor=white&style=flat) | Farmer-facing dashboard |

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy scikit-learn requests flask
```

### Setup

```bash
# Clone the repository
git clone https://github.com/your-username/kisan-mitra.git
cd kisan-mitra
```

Add your API keys to a `.env` file:

```env
WEATHER_API_KEY=your_weather_api_key
MARKET_API_KEY=your_agmarknet_or_data_gov_key
GROUNDWATER_API_KEY=your_cgwb_api_key
```

### Run

```bash
python app.py
```

Navigate to `http://localhost:5000` and enter your farm's location, soil type, and water availability to get personalized recommendations.

---

## 🌍 Impact & Use Cases

| Farmer Type | How Kisan Mitra Helps |
|-------------|----------------------|
| 🌾 **Small & Marginal Farmer** | Crop recommendations within their water budget; fair market price awareness |
| 💧 **Water-stressed Region Farmer** | Groundwater alerts prevent over-extraction; drought-resistant crop suggestions |
| 📦 **Cash Crop Grower** | Live mandi prices to time the best market and maximize profit |
| 🌧️ **Rain-fed Farmer** | Weather-integrated irrigation planning; no wasted manual watering |
| 🆕 **First-generation Farmer** | AI guidance replaces years of experience with data-driven decisions |

---

## 🗺 Roadmap

- [x] Real-time groundwater level integration
- [x] Crop market price updates
- [x] Weather forecast integration
- [x] Personalized crop recommendations
- [x] Irrigation management system
- [ ] Voice interface in Hindi and regional languages
- [ ] SMS-based advisory for feature phone users
- [ ] Satellite imagery for soil health analysis
- [ ] Crop disease detection via phone camera
- [ ] Integration with government e-NAM platform
- [ ] Community forum for farmer-to-farmer knowledge sharing
- [ ] Offline mode for low-connectivity rural areas

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---
