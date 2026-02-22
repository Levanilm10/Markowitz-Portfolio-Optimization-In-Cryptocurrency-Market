# Portfolio-Optimization-In-Cryptocurrency-Market
This project investigates systematic portfolio construction in the cryptocurrency market using constrained mean–variance optimization with a realistic risk controls and robustness improvements. 

The backtest is conducted over the period from January 2022 to January 2024.   
The investment universe consists of 20 liquid crypto-assets plus a cash position.  
Portfolio optimization is solved in CVXPY.


---

## Project overview

This project:
- Benchmarks simple strategies (Bitcoin-only, equal-weighted)
- Implements constrained Markowitz rebalancing
- Adds robustness layers to stabilize allocations:
  - Per-asset concentration cap
  - Transaction fees
  - Ledoit–Wolf Covariance shrinkage
  - diversification constraint

---

## Risk controls implemented

Throughout the backtest, we enforce realistic portfolio constraints, including a long-only allocation, an annualized volatility cap, and a global transaction-cost budget applied over the entire backtest horizon. Full definitions of these constraints, as well as all performance metrics (Sharpe ratio, maximum drawdown, diversification metric, etc.), are provided in the report.

---

## Repository contents

### Notebooks
- `Data_study.ipynb`  
  Data inspection.
- `Benchmark-bitcoin.ipynb`  
  Bitcoin-only benchmark.
- `Benchmark-equal_weights.ipynb`  
  Equal-weight benchmark.
- `Markowitz_without_x_max.ipynb`  
  Baseline constrained Markowitz.
- `Markowitz_x_max_only.ipynb`  
  Markowitz with per-asset cap `w_max`.
- `Markowitz_LedoitWolf.ipynb`  
  Markowitz with Ledoit–Wolf covariance shrinkage.
- `Markowitz_LedoitWolf_D_min.ipynb`  
  Markowitz with Ledoit–Wolf and diversification constraint (`D_min`).


### Report
- [Portfolio_optimization.pdf](./report.pdf)




