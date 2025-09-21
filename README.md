# 📈 Stock Screener

This project implements a **stock screener in Python** that leverages **mean reversion, momentum, and analyst ratings** to generate buy and sell signals for all stocks in the S&P 500.  

The trading algorithm combines **technical indicators** with **sentiment filters** to decide whether to **buy, sell, or hold** a stock. Performance is evaluated through backtesting against a standard buy-and-hold strategy.

---

## 🔑 Key Steps
- **Data Collection**: Retrieved market data using Yahoo Finance in Python.  
- **Technical Analysis**: Derived indicators (Bollinger Bands, RSI, MFI) through custom Python functions.  
- **Signal Logic**: Designed rules for buy/sell decisions based on mean reversion + momentum.  
- **Backtesting**: Compared algorithmic strategy returns against buy-and-hold benchmarks.  

---

## 🧮 Algorithm Logic

**Mean Reversion + Momentum Conditions**  

- **BUY**: `Low < Bollinger Band Lower` **AND** (`RSI < 30` **OR** `MFI < 20`)  
- **SELL**: `High > Bollinger Band Upper` **AND** (`RSI > 70` **OR** `MFI > 80`)  

---

## 📊 Interpretation & Examples

- **Example 1: TTD**  
  - Buy-and-hold: **$10,000 → $10,500** (+5%)  
  - Algorithm: **$10,000 → $31,917** (+219%)  
  - **Result**: Algorithm outperformed buy-and-hold by **214%**.  

- **Example 2: EPAM**  
  - Buy-and-hold: **$10,000 → $5,015**  
  - Algorithm: **$10,000 → $19,349** (+93.4%)  
  - **Result**: Significant outperformance compared to passive holding.  

---

## ✅ Conclusion

- **Top Performers**: TTD, EPAM, HAL  
- **Underperformers**: Hyper-growth stocks such as NVDA, SMCI, and PLTR  

**Key Insight**:  
Our algorithm excels in **volatile or range-bound markets**, where mean reversion and momentum capture short-term inefficiencies. However, it tends to **underperform on long-term hyper-growth stocks**, where buy-and-hold remains superior.
