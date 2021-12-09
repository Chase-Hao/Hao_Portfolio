---
date: "2021-11-01"
math: true
title: Backtrader framework learning
type: book
weight: 30
diagram: true
---

## Goal:
There are a few examples I write to test 'backtrader' and 'Pandas_TA' packages in python
- Use 'Backtrader' to test different types of datasets and strategies
- Use Pandas_TA to create different indicators
<br></br>
## Requirement
---
Backtrader
Pandas_TA
<br></br>
## Code detail
---
#### Backtrader
Need to redefine 'initial' function and trading related functions to fit different strategies and datasets.
1.  Test multi-timeframe strategy **e.g.** use '15mins average price line' and '1 hour average price line' in a same strategy
2.  Test multi-variable strategy **e.g.** combine out-source indicator like 'VIX' into initial dataset
