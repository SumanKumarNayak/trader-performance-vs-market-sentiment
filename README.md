# Trader Performance vs Market Sentiment Analysis

## Overview

This project analyzes the relationship between Bitcoin market sentiment (Fear/Greed Index) and trader behavior on Hyperliquid. The objective is to identify patterns in trader profitability and behavior across different sentiment regimes and derive actionable strategy insights.

---

## Objective

To evaluate how market sentiment (Fear vs Greed) impacts:

- Daily trader profitability (PnL)
- Win rate
- Trade frequency
- Position sizing
- Long/Short bias
- Segment-level performance differences

---

## Datasets Used

### 1. Bitcoin Market Sentiment (Fear/Greed Index)
- Columns: date, classification
- Used to classify each day into Fear or Greed regimes.

### 2. Historical Trader Data (Hyperliquid)
- Fields include: Account, Timestamp, Closed PnL, Size USD, Side, etc.
- Used to compute daily trader-level performance and behavioral metrics.

---

## Methodology

1. Converted trade timestamps (milliseconds) into proper datetime format.
2. Aggregated trade-level data into account-day level metrics:
   - Daily PnL
   - Win rate
   - Trade count
   - Average trade size
   - Long ratio
3. Simplified sentiment classifications into Fear and Greed groups.
4. Merged daily trader metrics with sentiment data.
5. Compared performance and behavior across Fear vs Greed regimes.
6. Created trader segments using median activity split (High vs Low Activity).
7. Evaluated how sentiment affects different trader segments.

---

## Key Insights

### 1. Traders Perform Significantly Better During Fear Periods

- Average daily PnL during Fear is more than 2x higher than during Greed.
- Median PnL is substantially higher during Fear.
- Win rate is also higher during Fear periods.

This suggests volatility-driven market conditions may create stronger short-term trading opportunities.

---

### 2. Trading Activity Increases Substantially During Fear

- Average trade count during Fear is approximately 3.5x higher than during Greed.

This indicates traders increase participation during volatile or panic-driven markets.

---

### 3. Increased Long Bias During Greed Does Not Improve Performance

- Long ratio is slightly higher during Greed.
- However, profitability and win rates do not improve accordingly.

This may suggest overconfidence or crowded positioning behavior during optimistic market phases.

---

### 4. Activity Amplifies Returns During Fear

- High-activity traders significantly outperform low-activity traders during Fear periods.
- Increased participation acts as a performance multiplier during volatile conditions.

---

## Strategy Recommendations

### Strategy 1 — Increase Activity During Fear Regimes

Given higher profitability and stronger performance among high-activity traders during Fear periods, increasing participation during volatility-driven market conditions may improve outcomes.

---

### Strategy 2 — Maintain Discipline During Greed Phases

Although traders exhibit stronger long bias during Greed periods, performance does not improve accordingly. Reducing directional bias and tightening risk management during Greed phases may enhance risk-adjusted returns.

---

## How to Run

1. Install Python (3.9+ recommended)
2. Install required libraries:

   pip install pandas matplotlib

3. Place both datasets in the same directory as the notebook.
4. Run:

   trader_performance_sentiment_analysis.ipynb

---

## Deliverables

- Jupyter Notebook with full analysis
- Visualizations comparing sentiment regimes
- Trader segmentation analysis
- Actionable strategy recommendations
