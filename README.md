# Statistical-Arbitrage-on-Gold-Silver-Pair-GoldBees-SilverBees-
Built a Statistical Arbitrage strategy on GoldBees–SilverBees using ADF tests, OLS hedge ratio (1.37), and Z-score mean reversion. Backtest over 35 months delivered 17.19% cumulative return, 0.87 Sharpe, and –6.42% max drawdown.
📘 Statistical Arbitrage on Gold–Silver Pair (GoldBees & SilverBees)

A mean-reversion based pairs trading strategy using ETFs with low tracking error.

📌 Project Overview

This project implements a complete Statistical Arbitrage (StatArb) pipeline on the Gold–Silver ETF pair (GoldBees & SilverBees by Nippon India).
The goal is to identify a stable long-term relationship between the two metal ETFs, construct a stationary spread, and trade mean reversion using a systematic long–short model.

I used 35 months of daily data (Feb 2022 – Feb 2025) sourced from Yahoo Finance.

🔍 Why GoldBees & SilverBees?

Selecting assets was the biggest challenge initially.
After comparing multiple options on the basis of tracking error, GoldBees and SilverBees stood out with one of the lowest tracking errors, making them highly suitable for StatArb.

🧠 Methodology
1. Data Collection

Source: Yahoo Finance

Timeframe: Feb 2022 – Feb 2025

Frequency: Daily

2. Correlation Analysis

Return correlation between Gold and Silver ETFs: 0.75

3. Hedge Ratio via OLS Regression

Regression: Silver = β × Gold

Estimated Hedge Ratio β = 1.37

4. Spread Construction
Spread
=
Silver
−
(
1.37
×
Gold
)
Spread=Silver−(1.37×Gold)
5. Stationarity Check (ADF Test)

Spread is stationary at 95% confidence, confirming long-term equilibrium (cointegration).

6. Trading Strategy (Mean Reversion)

Bands: 22-day moving average + 1.2 standard deviation

Rules:

Long when spread < lower band

Exit long at mean

Short when spread > upper band

Exit short at mean

📈 Backtest Results (Feb 2022 – Feb 2025)
Metric	Value
Cumulative Return	17.19%
Annual Return	5.56%
Annual Volatility	6.70%
Sharpe Ratio	0.87
Sortino Ratio	1.23
Max Drawdown	–6.42%
Omega Ratio	1.18
Longest Drawdown	218 days

A stable, low-volatility mean-reversion strategy suitable for educational and research purposes.
