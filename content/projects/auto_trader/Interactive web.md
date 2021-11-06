---
date: "2021-11-01"
math: true
title: Interactive Web
type: book
weight: 10
diagram: true
---

## Goal:
---
- Build a interactive web which can show up-to-date Bitcoin price
- Show my account balance, and add button to buy different cryptocurrency 
<br></br>
## Requirement
---
Binance API
flask web framework
<br></br>
## Code detail
---
1.  get hisotory bitcoin data and  from Binance 
2.  Use web-frame package 'flask' to construct web
  *   import tradingview lightweight chart js
  *   load historical data in data file
  *   fetch current data and add to the chart
  *   use binance API to post 'buy' order