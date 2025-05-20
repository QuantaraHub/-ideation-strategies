# Ideation-Strategies
A repo for brainstorming trading and research ideas.

## Structure
- `/ideas`: Trading and research ideas
- `/strategies`: Active and archived strategies
- `/docs`: Templates and guides
- `/meetings`: Brainstorming notes

# 📘 Intro

**Goal**: Alpha generation  
**Style**: Swing (several days)  
**Assets**: Equities/Crypto → Options (requires deeper modeling)  
**Data**: Yahoo Finance, Quandl, Alpaca, Binance, Polygon.io  
**Backtest Framework**: `backtrader` (for now)  
**Realism**: Include slippage, latency, fees  
**Grouping**: Based on confidence, score, or skill combo?

---

## ⚙️ Which Strategies?

1. **Mean Reversion**
2. **Momentum**
3. **Breakout Systems**
4. **Pairs Trading (Stat Arb)**
5. **Seasonal or Event-Based**

---

### 1. Mean Reversion

- **Assumption**: Prices revert to a mean (e.g., Bollinger Bands, RSI)  
- **Assets**: Range-bound equities, ETFs, FX  
- **Signals**: Stocks that deviate from historical average  
- **Pros**: High win rate, simple  
- **Cons**: Can underperform in trending markets

---

### 2. Momentum

- **Assumption**: Trends persist temporarily  
- **Techniques**: MA crossovers, relative strength, trend slope  
- **Signals**: Strong recent price trends (e.g., 20-day price change > 10%)  
- **Pros**: Works well in trending conditions  
- **Cons**: False breakouts, whipsaws

---

### 3. Breakout Systems

- **Approach**: Trade volatility expansions (e.g., Donchian Channels)  
- **Best for**: Crypto, futures, volatile stocks

---

### 4. Pairs Trading (Statistical Arbitrage)

- **Setup**: Long one asset, short another correlated one  
- **Signal**: Cointegration (e.g., Coke vs. Pepsi)  
- **Note**: Quant-heavy, market-neutral

---

### 5. Seasonal or Event-Based

- **Catalysts**: Earnings releases, Fed decisions, macro seasonality, index rebalancing

---

## 🧭 How to Find Trade Hypotheses for Equities

### Two Main Approaches:

- **Qualitative**: News, macro trends, sentiment, personal observation  
- **Quantitative**: Price/volume/volatility/statistical metrics

---

### Define Your Edge

- **Informational**: You know/see something others don't  
- **Analytical**: You interpret public info better  
- **Behavioral**: You act rationally when others panic  
- **Structural**: You exploit market inefficiencies

---

## 🔍 Qualitative Methods to Discover Trade Ideas

### 1. News-Driven (Momentum / Sentiment / Events)

- Alternative trend data (e.g., Twitter, Reddit)
- Market overreaction to economic or political events
- Regulatory changes
- Industry disruption (e.g., DeepSeek)
- CEO exits or scandals

### 2. Fundamentals

- M&A activity  
- Screen for value (low P/E)  
- Growth metrics (EPS, revenue)  
- Financial health (low debt, high ROE)  
- Upcoming catalysts (earnings, insider buying)

### 3. Qualitative Observation

- Buy what you know — full restaurants, emerging brands, tech adoption trends

### 4. Curiosity & Intuition

- “Why is no one talking about this?”  
- “What are people irrational about right now?”

### 5. Macro Thesis

- Top-down reasoning  
  - Example:  
    - Tariffs → higher VIX → gold up  
    - Rate hikes → bank earnings → REIT stress

---

## ✅ Final Filter Before Deep Analysis

| Factor              | Question                                                      |
|---------------------|---------------------------------------------------------------|
| Liquidity           | Is there enough daily volume for your strategy size?          |
| Volatility          | Is there enough movement to generate returns?                 |
| Information Flow    | Can you access fundamental or technical data easily?          |
| Catalysts           | Are there upcoming earnings, legal events, product launches?  |
| Strategy Fit        | Does the stock suit momentum, value, or stat-arb strategies?  |

---

# 🔬 Quantitative Screening to Filter Trading Ideas

Quantitative screening helps narrow thousands of assets to high-probability setups using data-aligned filters. Below are key screening goals and the metrics that support them.

### Strategy Goal → Core Filter

| Goal                         | Core Filters                             |
|------------------------------|------------------------------------------|
| Scalability                  | Liquidity & Execution                    |
| Trend-Following              | Momentum                                 |
| Counter-Trend Trades         | Mean Reversion + Volatility              |
| Market Inefficiencies        | Statistical + Correlation                |
| Macro/Behavioral Edge        | Event-Driven + Sentiment + Fundamentals  |
| Portfolio Quality Control    | Risk Metrics + Composite Ranking         |

---

## 📂 Screening Categories

1. Liquidity & Execution  
2. Momentum & Trend  
3. Mean Reversion & Volatility  
4. Statistical & Anomaly Detection  
5. Correlation & Pairs Trading  
6. Fundamental, Sentiment & Event  
7. Risk & Composite Ranking

---

### 1. Liquidity & Execution Filters

- **Average Daily Volume**: > 1M shares  
- **Dollar Volume**: > $5M/day  
- **Bid-Ask Spread**: < 0.5% of price  
- **Tick Size vs. Price**: < 0.1% of price  
- **Short Borrow Availability**: > 100k shares available (for short setups)

---

### 2. Momentum & Trend Filters

- **RSI (14)**: > 70  
- **Price Acceleration**: 20-day MA slope > 0; 5-day gain > 5%  
- **MACD Crossovers**: 12,26,9 configuration  
- **12-1 Momentum Strategy**: 12-month return > 20%, exclude last month  
- **Breakouts**: Price > 52-week high w/ volume > 1.5x average

---

### 3. Mean Reversion & Volatility Screens

- **Bollinger Bands**: Price outside 2 SD band  
- **Distance from MA**: Price >10% below 50-day SMA  
- **RSI Extremes**: RSI < 30 or > 70  
- **ATR**: > 1.5 = high volatility  
- **IV vs HV Spread**: Implied > Historical by 10%

---

### 4. Statistical & Anomaly Detection

- **Z-Score**: > 2 SD from mean  
- **P-Values**: < 0.05 (t-test on returns)  
- **Regression Residuals**: > 2 SD from trend  
- **Abnormal Volume/Volatility**: > 2x average

---

### 5. Correlation & Pairs Trading Signals

- **Cointegration Test**: p < 0.05  
- **Rolling Correlation**: > 0.8 over 60 days  
- **Spread Deviation**: Z-score > 2  
- **Beta-Neutral Stat Arb**: Hedge ratio-based divergence

---

### 6. Fundamental, Sentiment & Event Filters

- **Valuation**: P/E < 15, PEG < 1, ROE > 15%, D/E < 1  
- **Earnings Surprise**: > ±8%  
- **News Sentiment**: NLP score > 0.7  
- **Social Sentiment Shift**: Reddit/X delta > 15%  
- **Insider Buying**: > $1M in last 90 days  
- **Upcoming Catalysts**: Earnings, Fed dates, etc.

---

### 7. Risk & Composite Ranking Filters

- **Sharpe Ratio**: > 1.5  
- **Sortino Ratio**: > 2  
- **Calmar Ratio**: > 1  
- **Max Drawdown**: < 10%  
- **Alpha Score**:  
  `Alpha = 0.4 * Momentum + 0.3 * Volatility + 0.2 * Sentiment + 0.1 * Valuation`  
  _(Normalize each score to 0–1 and rank top candidates)_

**Tools:** Most trading platforms allow you to screen trades. You can also write a custom screener in Python, or use online tools like [QuantConnect](https://www.quantconnect.com/), [StockFetcher](https://www.stockfetcher.com/), [Koyfin](https://www.koyfin.com/), and [Quiver Quant](https://www.quiverquant.com/).

| **Tool**         | **Best For**                             |
|------------------|-------------------------------------------|
| **Finviz**       | Fast general screening (free)             |
| **TradingView**  | Visual/technical traders                  |
| **Yahoo Finance**| Beginners & long-term investors           |
| **QuantConnect** | Coders + backtesting                      |
| **Quiver Quant** | Sentiment + alternative data hunters      |
| **Koyfin**       | Fundamentals + macro visuals              |

