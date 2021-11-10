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
- Build an **interactive website** which can show up-to-date Bitcoin prices and account balance as well as buy and sell features
<br></br>
## Requirement
---
Binance API
flask web framework
<br></br>
## Code detail
---
1.  get historical bitcoin data and  from Binance 
2.  Use web-frame package 'flask' to construct web
  *   import lightweight chart js from Tradingview
  *   load historical data
  *   fetch current data and add to the chart
  *   use Binance API to post 'buy' order