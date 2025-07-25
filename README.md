This project is an intraday algorithmic trading bot built around Renko charts, designed for the Indian stock market (NSE). It supports live trading and backtesting using multiple strategies including momentum, scalping, and VWAP, with dynamic entry/exit logic and choppiness filters.

🔧 Features
📊 Renko Chart Generator: Converts price data into Renko bricks (renkoBrickGenerator.py).

📡 Live Data Streaming: Fetches and processes real-time candle data using WebSocket (DataFetcher.py).

📁 Persistent State: Uses Pickle/CSV/MySQL for saving state and restoring data across sessions (RestoreData.py, createDB.py).

🧠 Strategy Modules:

ScalperStockBot.py – Short-term scalping logic

VWAPStockBot.py – VWAP-based strategy

MasterBot.py – Central controller for multi-stock execution

📈 Plotting & UI:

Tkinter GUI for interactive visualization (gui.py, PlotGraph.py)

📦 Backtesting:

Multiple backtest modules for different strategies (BackTest.py, LongRunBackTest.py, VWAPStrategyBacktest.py, etc.)

🔐 Secure Login & Credentials Handling (login.py, credentials.py)

🧠 Strategy Logic
Monitors price change from session open

Uses Renko bricks on 3-minute candle closes

Calculates Choppiness Index for trend confirmation

Dynamic buy/sell decisions based on:

Breakout strength

Trend direction

Stoploss and target logic

Calculates charges, slippage, brokerage for accurate PnL

🧪 Backtesting Engine
Reads historical data (CSV)

Reconstructs Renko bricks offline

Applies the same logic used in live trading

Supports long-run and scalping-specific backtests

📌 Technologies
Python 3.11+

Asyncio & Threadding for concurrent stock tracking

Matplotlib for plotting

Pandas DF

MySQL + aiomysql for data storage

TKinter for UI

Fyers API V3 for market data (live & historical)
