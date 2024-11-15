# Alpaca API Trading Strategy

This project involves developing a statistical arbitrage trading strategy using the Alpaca Broker API. The focus is on optimizing a minimum variance portfolio composed of selected assets, with statistical arbitrage implemented on cointegrated pairs. The project combines data analysis, strategy formulation, and trading execution, aiming to maximize returns while minimizing risk through a carefully balanced asset allocation.

## Project Overview

### Objectives

- **Statistical Arbitrage**: Implement a pairs trading strategy by identifying cointegrated stock pairs.
- **Minimum Variance Portfolio**: Allocate assets (SPY, VOO, BND, and AAPL) to achieve minimum portfolio variance while adhering to the rules of statistical arbitrage.
- **Trade Execution**: Use Alpaca's API to manage and execute trades based on calculated asset weights and portfolio allocation.

### Key Results

- Achieved a minimum variance portfolio with optimized allocations:
  - **SPY**: 0 shares
  - **VOO**: 1252 shares
  - **BND**: 13 shares
  - **AAPL**: 3 shares
- Demonstrated profitability by assessing the performance through a generated "Tear Sheet," highlighting return metrics, volatility, and risk-adjusted performance of the pairs strategy.

## Methodology

### 1. Data Collection
   - Collected historical price data for selected assets (SPY, VOO, BND, AAPL) via the `yfinance` library.
   - Retrieved up-to-date asset data directly through Alpaca's API to synchronize trading actions.

### 2. Statistical Arbitrage on Cointegrated Pairs
   - Identified two pairs (e.g., MSFT-ADBE, ORCL-AMAT) with strong cointegration using statistical tests.
   - Applied mean reversion to determine entry and exit points based on pair spread deviations.

### 3. Minimum Variance Portfolio Optimization
   - Calculated returns for each asset and optimized portfolio weights to minimize overall portfolio variance using the `scipy.optimize.minimize` function.
   - Allocated assets based on the minimum variance results, focusing on the target allocations for each selected asset.

### 4. Trade Execution with Alpaca API
   - Executed trades based on the optimized portfolio weights through the Alpaca Broker API.
   - Automated buying of the calculated number of shares for each asset to maintain the desired portfolio allocation.

## Technical Stack

- **Programming Language**: Python
- **Libraries**: 
  - **Data Analysis**: `pandas`, `numpy`
  - **Optimization**: `scipy`
  - **Finance Data**: `yfinance`
  - **Visualization**: `matplotlib`
  - **API Interaction**: `requests`, `json`
- **APIs**: Alpaca Broker API for real-time trading
- **Concepts**: Minimum Variance Portfolio, Cointegration, Mean Reversion, Statistical Arbitrage
