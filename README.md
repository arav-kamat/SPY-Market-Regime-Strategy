# SPY Market Regime Strategy

A Python-based quantitative trading strategy that identifies U.S. market regimes using a 3-state Hidden Markov Model (HMM) and implements dynamic, regime-aware portfolio allocation on SPY. The strategy combines early-warning technical indicators, momentum and volatility signals, and position sizing rules to optimize returns while managing risk.

## Features

- **Market Regime Detection:** Uses a 3-state Gaussian HMM to label Bull, Bear, and Sideways regimes.
- **Early Warning Indicators:**  
  - Trend Exhaustion (EMA 3/8 crossover)  
  - Volatility Breakout (5-day realized volatility vs 20-day average)  
  - Breadth Deterioration (SPY vs 50-day SMA)  
  - Momentum Divergence (RSI near highs)
- **Dynamic Position Sizing:** Scale positions daily (0–150% long or short) based on regime and indicator scores.
- **Portfolio Backtesting:** Tracks portfolio value, daily returns, and enforces yearly drawdown limits.
- **Performance Metrics:** Sharpe ratio, cumulative returns, and comparison against SPY buy-and-hold.
- **Visualization:** Overlay market regimes on SPY price charts and highlight portfolio performance.
- **Leverage Support:** Apply leverage in confirmed bull regimes to maximize gains.

## Installation

Clone the repository:

```bash
git clone https://github.com/arav-kamat/SPY-Market-Regime-Strategy.git
cd SPY-Market-Regime-Strategy
