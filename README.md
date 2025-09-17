
---

## 📊 Objective
Analyze how trading behavior (profitability, risk, volume, leverage) aligns with Bitcoin market sentiment (**Fear vs Greed**) to uncover patterns that could inform smarter trading strategies.  

---

## 📁 Datasets
1. **Historical Trader Data (Hyperliquid)**  
   - ~211,000 trades  
   - Columns: `account`, `symbol`, `execution price`, `size`, `side`, `closedPnL`, `leverage`, etc.  

2. **Bitcoin Fear & Greed Index**  
   - ~2,600 records  
   - Columns: `date`, `classification (Fear/Greed)`, `value`.  

---

## 🧹 Data Processing
- Standardized and cleaned numeric + categorical fields.  
- Converted `Timestamp IST` into `trade_time` and `trade_date`.  
- Mapped sentiment classes into **Fear** and **Greed**.  
- Merged both datasets on daily date.  

---

## 🔎 Analysis & Insights
- **Profitability (Closed PnL):**  
  No statistically significant difference between Fear vs Greed days (t-test p ≈ 0.32).  

- **Trading Activity:**  
  Volume of trades spikes during extreme sentiment days.  

- **Trade Size:**  
  Different spread distributions across Fear vs Greed.  

- **Implication:**  
  Sentiment doesn’t directly predict profit, but acts as a signal of market activity conditions useful for risk management.  

---

## 📈 Visual Outputs
- `closedpnl_by_sentiment.png` → PnL distribution across sentiment.  
- `trade_size_by_sentiment.png` → Trade size violin plots.  
- `trades_per_day_by_sentiment.png` → Daily trades by sentiment.  

---

## 📄 Report
See [`ds_report.pdf`](./ds_report.pdf) for detailed write-up of methodology, results, and conclusions.  

---

## ▶️ How to Run
1. Open [`notebook_1.ipynb`](./notebook_1.ipynb) in **Google Colab**.  
2. Make sure runtime = Python 3.  
3. Run all cells → this will:  
   - Download datasets from provided Google Drive links.  
   - Perform cleaning, merging, and analysis.  
   - Save visualizations in `outputs/`.  
   - Export results into `csv_files/` and `ds_report.md`.  

📌 Colab Link (view-only): (https://colab.research.google.com/drive/1mHifMsd19zIcxn1DklybzrWgDu5WqJQb?usp=sharing)]  

---

## ✅ Submission Compliance
- Google Colab notebook provided (public, view-only).  
- Repo structure matches instructions.  
- `ds_report.pdf` included.  
- Outputs + CSVs stored in correct folders.  

---
