---
date: "2021-11-01"
math: true
title: Auto-Trading bot
type: book
weight: 10
diagram: true
---
## Goal:
---
- Code to realize auto-trading under a strategy
<br></br>
## Requirement
---
CXCT: framework combining different platforms' API
<br></br>
## Code detail
---
Use CXCT framework to get different platform API: cryptocurrency platform API
* log in to one of the cryptocurrency platforms
* fetch 15mins candle sticks data
* build strategy, create a signal to buy and sell
* when the signal occurs, buy or sell at market value
* set schedule to run it every 15 minutes