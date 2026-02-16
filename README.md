# 🤖 AI-Powered Stock & ETF Signal Generation Platform


A comprehensive trading signal platform that combines **Machine Learning
(Random Forest + XGBoost + LSTM)** with **Technical Analysis (RSI, MACD, SMA)**
to generate high-confidence stock predictions.

The platform features a modern glassmorphism dashboard, smart email
alerts, and a resilient microservices architecture.

------------------------------------------------------------------------

# 🚀 Quick Start

## ✅ Windows (Recommended)

```powershell
streamlit run 0_Overview.py
```

This script automatically:

- Starts the ML Signals API

- Starts the Alerts Service

- Starts the Backtesting Engine

- Launches the Streamlit Dashboard

------------------------------------------------------------------------

## ⚙️ Manual Start

### Terminal 1 -- Start ML Signals API

``` bash
python signals/api.py
```

### Terminal 2 -- Start Alerts Service

``` bash
python alerts/main.py
```

### Terminal 3 -- Start Backtesting Engine

``` bash
python backtesting/main.py
```

### Terminal 4 -- Start Dashboard

``` bash
streamlit run 0_Overview.py
```

------------------------------------------------------------------------

## 🌐 Access Points

-   📊 Dashboard: http://localhost:8501
-   📡 ML Signals API: http://localhost:8000
-   🔔 Alerts Service: http://localhost:8001
-   🧪 Backtesting Engine: http://localhost:8002

------------------------------------------------------------------------

# 💎 Key Features

## 🧠 Hybrid AI Architecture

-   Random Forest, XGBoost & LSTM models
-   5 years of historical training data
-   Technical validation via RSI, MACD, SMA, EMA
-   Explainable AI reasoning per signal

## 🖥️ Modern Dashboard

-   Glassmorphism UI
-   Dark Mode
-   Real-Time Price Updates
-   Interactive Technical Charts

## 🛡️ Resilience & Safety

-   Circuit breakers
-   Smart fallback system
-   No-flicker signal stability
-   Graceful API failure handling

## 🔔 Smart Alerts

-   HTML formatted email alerts
-   Confidence score included
-   Signal strength level
-   Scheduled & Instant reports

------------------------------------------------------------------------

# 🏛️ Architecture Overview

Frontend (Streamlit) ↔ Backend API (FastAPI) ↔ ML Engine\
Alerts Service runs independently for scheduled notifications.

------------------------------------------------------------------------

# 📡 Core API Endpoints

## Live Prediction

POST /api/v1/ml/signal/live

## Historical Signals

POST /api/v1/ml/signal/historical

## Market Data

GET /supabase/recent/{ticker}
GET /supabase/ticker/{ticker}

## Market Overview

GET /supabase/latest
GET /supabase/top-performers

## Analysis

GET /supabase/stats/{ticker}
GET /supabase/rsi-search

------------------------------------------------------------------------

# ⚡ System Flow

1.  User enters ticker
2.  Data fetched via yfinance
3.  ML models generate probability
4.  Technical rules validate trend
5.  Hybrid signal produced
6.  Backtesting validates the signal
7.  Dashboard displays result
8.  Alerts sent (if configured)

------------------------------------------------------------------------

# 🤖 Running Ollama

## Install

https://ollama.com/download

## Pull Model (First Time)

``` bash
ollama pull mistral
```

## Start Server

``` bash
ollama serve
```

## Test Model

``` bash
ollama run mistral
```

------------------------------------------------------------------------

# 📜 License

MIT License
