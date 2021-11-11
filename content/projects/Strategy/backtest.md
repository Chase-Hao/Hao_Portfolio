---
date: "2021-11-01"
math: true
title: Light-weight backtest
type: book
weight: 20
diagram: true
---

## Goal:
---
- Backtest a given strategy and analyze its performance
-  Find the optimal input number for a given strategy and test its robustness
<br></br>
## Requirement
---
Pandas_TA
<br></br>
## Code detail
It tests the Momentum factor using the 'moving average' technical indicator as an example
1. Iterate different numbers to identify the pair which can generate the most profit
2. For a given strategy, randomly select 100 samples from the original data to test the robustness.