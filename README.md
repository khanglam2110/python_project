# 📊 VN30 Spillover Effect & Network Analysis

## 📌 Overview
This project analyzes the spillover effects and interconnectedness among stocks in the VN30 index using a Vector AutoRegression (VAR) framework and Forecast Error Variance Decomposition (FEVD).

The goal is to uncover:
- How shocks propagate across stocks
- Which stocks act as risk transmitters or receivers
- The overall systemic risk structure of the Vietnamese stock market

--- 

## 📊 Data
- Source: VN30 stock price data collected in Investing.com
- Period: 2020-2025
- Preprocessing:
  - Cleaned and formatted raw data in Excel
  - Calculated log returns
  - Conducted stationary tests

--- 

## ⚙️ Methodology 
1. Data Processing
- Source: VN30 stock price data (2020-2025)
- Cleaned ticker symbols and standardized format
- Converted to log returns

2. Stationarity Check
- Applied Augmented Dickey-Fuller (ADf) test
- Ensured suitability for VAR modeling

3. VAR Model
- Selected optimal lag using AIC
- Imposed minimum lag (≥1) to capture dynamic relationships

4. FEVD & Spillover Matrix
- Used FEVD to decompose forecast error variance
- Constructed spillover matrix representing cross-stock influence

5. Spillover Metrics
- Total Spillover Index (TSI)
- Directional Spillover (TO, FROM, NET)

6. Network Analysis
- Built a directed network graph
- Nodes represent stocks
- Edges represent spillover effects
- Node size = magnitude of net spillover
- Node color:
  - 🔴 Transmitters (NET > 0)
  - 🔵 Receivers (NET < 0)

--- 

## 📈 Key Results
🔥 Total Spillover Index
TSI = 39.85%

This indicates a moderately high level of interconnectedness, suggesting that shocks are significantly transmitted across stocks in the VN30 market.

🧠 Network Structure
- The network exhibits a core-periphery structure
- A small number of stocks play a central role in absorbing shocks
- Many stocks act as sources of volatility

--- 

## 🏦 Key Insight: 
Dominant Receiver
- ACB emerges as a major hub
- It absorbs spillover from a wide range of stocks

  👉 ACB plays a critical role in the system, acting as a central node in the risk transmission network. 

🔴 Transmitters vs 🔵 Receivers
- Majority of stocks are net transmitters
- Only a few act as net receivers

  👉 This suggests risk is distributed widely but absorbed selectively, leading to concentration of systemic pressure.

🧲 Sector Dynamics
- Banking stocks form the core cluster of the network
- Strong interconnections within the financial sector

  👉 The financial sector plays a key role in driving and absorbing market-wide shocks.

--- 

## ⚡ Implications
- High spillover → limited diversification benefits
- Presence of central nodes → systemic risk concentration
- Monitoring key stocks (e.g., ACB) is critical for risk management

---

## 🚀 Future Improvements
- Rolling spillover analysis (time-varying dynamics)
- Sector-level aggregation
- Centrality-based ranking of systemic importance
- Integration with portfolio risk models

---

## 🧩 Tech Stack
- Python
- Pandas, NumPy
- Statsmodels (VAR, FEVD)
- NetworkX
- Matplotlib 

---

📎 Conclusion
This project demonstrates how combining econometric modeling and network analysis can provide deeper insights into market structure and systemic risk.
It highlights the importance of identifying key nodes in financial networks and understanding how shocks propagate across assets. 









