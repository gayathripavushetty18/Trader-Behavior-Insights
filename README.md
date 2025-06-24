# Trader-Behavior-Insights
Analyzed the impact of Bitcoin market sentiment (Fear/Greed) on trader performance using Hyperliquid data. Mapped sentiment to trades by date, explored PnL patterns, and visualized behavioral trends. Revealed how emotional sentiment influences trading outcomes in crypto markets.
# 🧠 Trader Behavior vs Market Sentiment – Data Science Task

## 📌 Objective

The goal of this project is to explore the relationship between **trader performance** and **Bitcoin market sentiment**, using two datasets:
1. **Bitcoin Market Sentiment Dataset** – Shows market sentiment (Fear/Greed) by date.
2. **Historical Trader Data from Hyperliquid** – Contains trader-level transaction data including execution price, size, PnL, and timestamps.

This analysis aims to uncover patterns between emotional sentiment in the crypto market and actual trading performance to help drive smarter trading strategies.

---

## 🗂️ Datasets Used

### 1. Bitcoin Market Sentiment Dataset
- Columns: `date`, `classification` (`Fear`, `Greed`, `Extreme Greed`, etc.)

### 2. Historical Trader Data (Hyperliquid)
- Columns used:
  - `Account`
  - `Coin`
  - `Execution Price`
  - `Size Tokens`
  - `Side`
  - `Timestamp IST`
  - `Start Position`
  - `Direction`
  - `Closed PnL`

---

## 🧹 Data Preprocessing

- Parsed human-readable `Timestamp IST` from trader data to extract `date`
- Cleaned sentiment data by removing rows with missing or invalid dates
- Mapped sentiment classifications to trader data by date

---

## 📊 Analysis Performed

1. **Mapped sentiment to each trade** based on the trade date.
2. **Grouped trades by sentiment** to compare average `Closed PnL`, trade sizes, and frequency.
3. **Visualized profit/loss distributions** using a boxplot:

![Closed PnL Distribution](e6c84aac-e103-4820-a235-d4fc150d4001.png)

### 📈 Key Insight:
- Trades executed during `Greed` and `Extreme Greed` days show wider variance in PnL, indicating more risk-taking behavior.
- During `Extreme Fear`, most trades show tighter distributions, suggesting cautious trading.

---

## 🛠️ Tech Stack

- Language: Python 3.9+
- Libraries: `pandas`, `matplotlib`, `seaborn`

---

## 📂 Files Included

- `notebook.ipynb` – Jupyter notebook with all code
- `fear_greed_index.csv` – Market sentiment data
- `historical_trader_data.csv` – Trader performance data
- `README.md` – Project documentation

---

## ✅ How to Run

1. Clone the repo
2. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn
