# 🚀 DEPTHOS



### Institutional-Style Gate.io Market-Making Infrastructure for Low-Nominal Perpetuals

> **Multi-ticker execution engine for Gate.io perpetual futures with market data, OMS, risk controls, reconciliation, backtesting, observability, and API-ready architecture.**

---

## ✨ Overview

**MarketForge** is a modular Python trading infrastructure project built for **Gate.io USDT perpetual futures**.

It is designed for **low-nominal contracts**, **multi-ticker market making**, and **execution-aware research workflows**. The system combines live market data handling, order lifecycle management, risk controls, reconciliation, backtesting, and observability into one structured codebase.

This project is best positioned as:

- 💼 **White-label trading infrastructure**
- 🧠 **Execution engine foundation**
- 🏗️ **SaaS-ready backend for trading products**
- 📊 **Research + paper/live deployment framework**
- ⚙️ **Advanced crypto market-making codebase**

---

## 🔥 Core Features

### 📡 Market Data
- Real-time WebSocket market data integration
- Order book / depth cache handling
- Trade tape processing
- Funding and mark price caches
- Candle service support
- Staleness detection

### 🧾 Order Management System (OMS)
- Structured order lifecycle state tracking
- Ack / replace / cancel flows
- Fill processing
- Client order registry
- Execution service abstraction
- Persistent order storage

### 💼 Portfolio & Positioning
- Position manager
- Inventory manager
- Exposure manager
- PnL tracking
- Account reconciliation hooks

### 🛡️ Risk Controls
- Kill switch support
- Connectivity guard
- Market regime guard
- Stale order guard
- Protective exit logic
- Centralized risk manager

### 🧠 Strategy Layer
- Fair value engine
- Alpha model scaffolding
- Inventory skew logic
- Spread model
- Quote sizing
- Reservation price logic
- Adverse selection filters
- Quote engine

### 🔄 Reconciliation & Recovery
- Startup reconciliation
- Periodic reconciliation
- Ghost order detection
- Orphan position detection
- Recovery actions framework

### 🧪 Backtesting & Replay
- Execution-aware backtest framework
- Queue model
- Fill model
- Slippage model
- Replay engine
- Reporting and metrics support

### 📈 Observability
- Metrics collection
- Health endpoints
- Alerts
- Audit logging
- Event logging
- Tracing hooks

### 🌐 API Layer
- Health routes
- Metrics routes
- Position routes
- Order routes
- Dashboard routes
- Embedded API server structure

---

## 🧱 Architecture

```text
MarketForge
├── app/
│   ├── api/               # Dashboard + service API
│   ├── backtest/          # Replay, fills, slippage, reports
│   ├── connectors/        # Gate.io REST + WebSocket integrations
│   ├── core/              # Shared infra utilities
│   ├── market_data/       # Books, trades, candles, marks, funding
│   ├── observability/     # Metrics, alerts, audit/event logs
│   ├── oms/               # Order lifecycle + execution services
│   ├── persistence/       # SQLite repositories and models
│   ├── portfolio/         # Positions, inventory, PnL, exposure
│   ├── reconcile/         # Startup and periodic exchange sync
│   ├── risk/              # Guards, limits, protective controls
│   ├── strategy/          # Alpha, fair value, spread, skew, sizing
│   └── main.py            # Main application entrypoint
├── scripts/               # Run live / paper / replay
├── tests/                 # Unit tests for critical logic
├── requirements.txt
└── README.md
