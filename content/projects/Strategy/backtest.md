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
-  Find the optimal input number for a certain strategy and test its robustness
<br></br>
## Requirement
---
Pandas_TA
<br></br>
## Code detail
1. For average line strategy, iterate different numbers to identify the pair which can generate the most profit
2.  For a certain strategy, randomly select 100 samples from original data to test the robustness.